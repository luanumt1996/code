
function cswp_maintenance_mode(){
    if(!current_user_can('edit_themes') || !is_user_logged_in()){
        wp_die('<h1 style="color:red">Bảo trì hệ thống</h1><br />Hiện tại chúng tôi đang bảo trì để nâng cấp hệ thống. Vui lòng quay lại sau ít phút!');
    }
}
add_action('get_header', 'cswp_maintenance_mode');
