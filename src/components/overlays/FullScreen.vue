<script>
// root emit event for full screen
import Icons from '../../stuff/icons.json'

export default {
    name: 'FullScreen',
    methods: {
        meta_info() {
            return { author: 'Fistevada', version: '0.1.0' }
        },
        tool() {
            return {
                // Descriptor for the tool
                icon: Icons['fullscreen.png'],
                hint: 'This hint will be shown on hover',
                data: [],     // Default data
                settings: {}, // Default settings
            }
        },
        use_for() { return ['FullScreen'] },
        data_colors() { return [this.color] }
    },
    // Define internal setting & constants here
    computed: {
        sett() {
            return this.$props.settings
        },
        color() {
            return this.sett.color || '#42b28a'
        },
        // Settings starting with $ are reserved
        selected() {
            return this.$props.settings.$selected
        },
        state() {
            return this.$props.settings.$state
        },
    },
    data() {
        return {}
    },

}
</script>
