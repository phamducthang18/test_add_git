<template>
    <div class="login-page">
        <div class="container">Login Page</div>
        <form class="form-container">
            <div class="form-group">
                <label for="email" class="label">Email</label>
                <input type="email" id="email" class="input">
            </div>
            <div class="form-group">
                <label for="password" class="label">Password</label>
                <input type="password" id="password" class="input">
            </div>
            <button type="submit" class="submit-button">Login</button>
        </form>
    </div>
</template>

<style scoped>
.login-page {
    max-width: 400px;
    
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    
}

.container {
    font-size: 30px;
    margin-bottom: 10px;
    text-align: center;
}

.form-container {
    display: flex;
    flex-direction: column;
    gap: 15px;
}

.form-group {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
}

.label {
    font-size: 20px;
    width: 100px; /* Đảm bảo chiều rộng đủ lớn để nhãn nằm thẳng hàng */
}

.input {
    font-size: 16px;
    flex: 1; /* Cho phép ô nhập liệu chiếm toàn bộ chiều rộng còn lại */
    padding: 5px;
    border-radius: 5px;
    border: 1px solid #ccc;
    box-sizing: border-box;
    outline: none;
    margin-left: 10px; /* Khoảng cách giữa nhãn và ô nhập liệu */
}

.submit-button {
    font-size: 18px;
    padding: 10px;
    border: none;
    border-radius: 5px;
    background-color: #089E0D;
    color: #fff;
    cursor: pointer;
    text-align: center;
    width: 100%;
}

.submit-button:hover {
    background-color: #28B02D;
}
</style>
