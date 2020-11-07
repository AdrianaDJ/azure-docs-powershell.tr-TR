---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 30ff5f7d9ead2226c6c03b4707af9c20ff40d405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917824"
---
# <span data-ttu-id="49db0-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="49db0-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="49db0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49db0-102">SYNOPSIS</span></span>
<span data-ttu-id="49db0-103">Yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="49db0-103">Registers a new user.</span></span>

## <span data-ttu-id="49db0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49db0-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49db0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="49db0-105">DESCRIPTION</span></span>
<span data-ttu-id="49db0-106">**Yeni-Azsız Kullanıcı** cmdlet 'i yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="49db0-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="49db0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49db0-107">EXAMPLES</span></span>

### <span data-ttu-id="49db0-108">Örnek 1: yeni bir kullanıcıyı kaydettirme</span><span class="sxs-lookup"><span data-stu-id="49db0-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="49db0-109">Bu komut, Patti Fuller adlı yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="49db0-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="49db0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49db0-110">PARAMETERS</span></span>

### <span data-ttu-id="49db0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="49db0-111">-Context</span></span>
<span data-ttu-id="49db0-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="49db0-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49db0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49db0-113">-DefaultProfile</span></span>
<span data-ttu-id="49db0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49db0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49db0-115">-E-posta</span><span class="sxs-lookup"><span data-stu-id="49db0-115">-Email</span></span>
<span data-ttu-id="49db0-116">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="49db0-116">Specifies the email address of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49db0-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="49db0-117">-FirstName</span></span>
<span data-ttu-id="49db0-118">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49db0-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="49db0-119">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="49db0-119">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49db0-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="49db0-120">-LastName</span></span>
<span data-ttu-id="49db0-121">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49db0-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="49db0-122">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="49db0-122">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49db0-123">Not</span><span class="sxs-lookup"><span data-stu-id="49db0-123">-Note</span></span>
<span data-ttu-id="49db0-124">Kullanıcı hakkında bir Not belirtir.</span><span class="sxs-lookup"><span data-stu-id="49db0-124">Specifies a note about the user.</span></span>
<span data-ttu-id="49db0-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="49db0-125">This parameter is optional.</span></span>
<span data-ttu-id="49db0-126">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="49db0-126">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49db0-127">-Parola</span><span class="sxs-lookup"><span data-stu-id="49db0-127">-Password</span></span>
<span data-ttu-id="49db0-128">Kullanıcı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49db0-128">Specifies the user password.</span></span>
<span data-ttu-id="49db0-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="49db0-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49db0-130">Durumlu</span><span class="sxs-lookup"><span data-stu-id="49db0-130">-State</span></span>
<span data-ttu-id="49db0-131">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="49db0-131">Specifies the user state.</span></span>
<span data-ttu-id="49db0-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="49db0-132">This parameter is optional.</span></span>
<span data-ttu-id="49db0-133">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="49db0-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49db0-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="49db0-134">-UserId</span></span>
<span data-ttu-id="49db0-135">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="49db0-135">Specifies the user ID.</span></span>
<span data-ttu-id="49db0-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="49db0-136">This parameter is optional.</span></span>
<span data-ttu-id="49db0-137">Bu parametre belirtilmezse, bu cmdlet bir kullanıcı KIMLIĞI oluşturur.</span><span class="sxs-lookup"><span data-stu-id="49db0-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49db0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49db0-138">CommonParameters</span></span>
<span data-ttu-id="49db0-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49db0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49db0-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49db0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49db0-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49db0-141">INPUTS</span></span>

### <span data-ttu-id="49db0-142">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="49db0-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="49db0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="49db0-143">System.String</span></span>

### <span data-ttu-id="49db0-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="49db0-144">System.Security.SecureString</span></span>

### <span data-ttu-id="49db0-145">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuserstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="49db0-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="49db0-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49db0-146">OUTPUTS</span></span>

### <span data-ttu-id="49db0-147">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="49db0-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="49db0-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49db0-148">NOTES</span></span>

## <span data-ttu-id="49db0-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49db0-149">RELATED LINKS</span></span>

[<span data-ttu-id="49db0-150">Get-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="49db0-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="49db0-151">Set-Azapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="49db0-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


