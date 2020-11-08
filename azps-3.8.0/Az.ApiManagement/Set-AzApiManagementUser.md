---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: a70cc953da853fd07dcee835f5a97a0efd2f6406
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104168"
---
# <span data-ttu-id="245eb-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="245eb-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="245eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="245eb-102">SYNOPSIS</span></span>
<span data-ttu-id="245eb-103">Kullanıcı ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="245eb-103">Sets user details.</span></span>

## <span data-ttu-id="245eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="245eb-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="245eb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="245eb-105">DESCRIPTION</span></span>
<span data-ttu-id="245eb-106">**Set-Azapsananagementuser** cmdlet 'i Kullanıcı ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="245eb-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="245eb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="245eb-107">EXAMPLES</span></span>

### <span data-ttu-id="245eb-108">Örnek 1: kullanıcının parolasını, e-posta adresini ve durumunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="245eb-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="245eb-109">Bu komut yeni bir Kullanıcı parolası ve e-posta adresi ayarlar ve kullanıcıyı engeller.</span><span class="sxs-lookup"><span data-stu-id="245eb-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="245eb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="245eb-110">PARAMETERS</span></span>

### <span data-ttu-id="245eb-111">-Context</span><span class="sxs-lookup"><span data-stu-id="245eb-111">-Context</span></span>
<span data-ttu-id="245eb-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="245eb-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="245eb-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="245eb-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="245eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="245eb-114">-DefaultProfile</span></span>
<span data-ttu-id="245eb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="245eb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="245eb-116">-E-posta</span><span class="sxs-lookup"><span data-stu-id="245eb-116">-Email</span></span>
<span data-ttu-id="245eb-117">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="245eb-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="245eb-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="245eb-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="245eb-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="245eb-119">-FirstName</span></span>
<span data-ttu-id="245eb-120">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="245eb-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="245eb-121">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="245eb-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="245eb-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="245eb-122">-LastName</span></span>
<span data-ttu-id="245eb-123">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="245eb-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="245eb-124">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="245eb-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="245eb-125">Not</span><span class="sxs-lookup"><span data-stu-id="245eb-125">-Note</span></span>
<span data-ttu-id="245eb-126">Kullanıcı hakkında bir Not belirtir.</span><span class="sxs-lookup"><span data-stu-id="245eb-126">Specifies a note about the user.</span></span>
<span data-ttu-id="245eb-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="245eb-127">This parameter is optional.</span></span>
<span data-ttu-id="245eb-128">Bu parametrenin varsayılan değeri $null.</span><span class="sxs-lookup"><span data-stu-id="245eb-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="245eb-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="245eb-129">-PassThru</span></span>
<span data-ttu-id="245eb-130">geçiş</span><span class="sxs-lookup"><span data-stu-id="245eb-130">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245eb-131">-Parola</span><span class="sxs-lookup"><span data-stu-id="245eb-131">-Password</span></span>
<span data-ttu-id="245eb-132">Kullanıcı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="245eb-132">Specifies the user password.</span></span>
<span data-ttu-id="245eb-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="245eb-133">This parameter is optional.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245eb-134">Durumlu</span><span class="sxs-lookup"><span data-stu-id="245eb-134">-State</span></span>
<span data-ttu-id="245eb-135">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="245eb-135">Specifies the user state.</span></span>
<span data-ttu-id="245eb-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="245eb-136">This parameter is optional.</span></span>
<span data-ttu-id="245eb-137">Varsayılan değer etkindir.</span><span class="sxs-lookup"><span data-stu-id="245eb-137">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245eb-138">-UserID</span><span class="sxs-lookup"><span data-stu-id="245eb-138">-UserId</span></span>
<span data-ttu-id="245eb-139">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="245eb-139">Specifies the user ID.</span></span>
<span data-ttu-id="245eb-140">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="245eb-140">This parameter is required.</span></span>

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

### <span data-ttu-id="245eb-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="245eb-141">-Confirm</span></span>
<span data-ttu-id="245eb-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="245eb-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="245eb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="245eb-143">-WhatIf</span></span>
<span data-ttu-id="245eb-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="245eb-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="245eb-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="245eb-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="245eb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245eb-146">CommonParameters</span></span>
<span data-ttu-id="245eb-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="245eb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245eb-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="245eb-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245eb-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="245eb-149">INPUTS</span></span>

### <span data-ttu-id="245eb-150">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="245eb-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="245eb-151">System. String</span><span class="sxs-lookup"><span data-stu-id="245eb-151">System.String</span></span>

### <span data-ttu-id="245eb-152">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="245eb-152">System.Security.SecureString</span></span>

### <span data-ttu-id="245eb-153">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuserstate</span><span class="sxs-lookup"><span data-stu-id="245eb-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="245eb-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="245eb-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="245eb-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="245eb-155">OUTPUTS</span></span>

### <span data-ttu-id="245eb-156">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="245eb-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="245eb-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="245eb-157">NOTES</span></span>

## <span data-ttu-id="245eb-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="245eb-158">RELATED LINKS</span></span>

[<span data-ttu-id="245eb-159">Get-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="245eb-159">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="245eb-160">Yeni-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="245eb-160">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="245eb-161">Remove-Azapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="245eb-161">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


