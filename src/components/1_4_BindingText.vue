<template>
    <div class="binding">
        <h1>{{ msg }}</h1>
        <div>Hello {{ name }}</div>
        <div v-html="channel"></div>
        <h2 :id="headingId">Heading</h2>
        <button :disabled="isDisabled">Bind</button>
        <h2 class="underline">Underlined Text</h2>
        <h2 class="underline" :class="status">Status</h2>
        <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
        <h2 :class="isSoldout ? 'sold-out' : 'new'">Soldout? Movie</h2>
        <h2 :class="['new', 'promoted']">Newly Promoted Movie</h2>
        <h2 :class="[isPromoted && 'promoted', isSoldout ? 'sold-out' : 'new']">Array Condition Movie</h2> 
        <h2 :class="{
        promoted: isPromoted,
        new: !isSoldout,
        'sold-out': isSoldout,
        }">Object Conditional Movie</h2>
        <h2 :style="{
            color: highlightColor,
            'font-size': headerSize + 'px',
            fontSize: headerSize + 'px',
            padding: '20px',
        }">Inline Style</h2>
        <h2 :style="headerStyleObject">Style Object</h2>
        <div :style="[baseStyleObject, successStyleObject]">Success Style</div>
        <div :style="[baseStyleObject, dangerStyleObject]">Danger Style</div>
    </div>
</template>

<script>
    export default {
        name: 'Binding',
        props: {
            msg: String
        },
        data() {
            return {
            name: "Batman",
            channel: "<strong>Codevolution</strong>",
            headingId: "heading",
            isDisabled: true,
            status: "danger",
            isPromoted: true,
            isSoldout: true,
            highlightColor: "orange",
            headerSize: 50,
            headerStyleObject: {
                color: "orange",
                fontSize: "50px",
                padding: "20px"
            },
            baseStyleObject: {
                fontSize: "50px",
                padding: "10px",
            },
            successStyleObject: {
                color: "green",
                backgroundColor: "lightgreen",
                border: "1px solid green",
            },
            dangerStyleObject: {
                color: "darkred",
                backgroundColor: "red",
                border: "1px solid dardred",
            },
        };
    },
}
</script>