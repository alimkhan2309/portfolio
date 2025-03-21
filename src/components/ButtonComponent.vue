
    <template>
        <button :class="buttonClass">{{ text }}</button>
    </template>

<script >
export default {
  props: {
    text: String,
    buttonStyle: {
        type: String,
        default: "primary"
    },
  },
  computed: {
    buttonClass() {
        return {
            primary: this.buttonStyle === "primary",
            secondary: this.buttonStyle === "secondary"
        }
    }
  }
};
</script>

<style scoped lang="css">
button {
    width:fit-content;
    font-size:16px;
    color: var(--black);
    padding: 14px 24px;
    border-radius: 6px;
}

.primary {
    background-color: var(--green);
    border: 0px;
    font-size: var(--body);
    font-weight: bold;
}
.secondary {
    color: var(--light-gray);
    background-color: none;
    border: 1px;
    border-color: var(--light-gray);
    font-size: var(--body);
    font-weight: bold;
}

</style>