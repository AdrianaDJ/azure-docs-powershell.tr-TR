---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: 03ea39c24166b6e44c057907fbc7346996d3dfa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917656"
---
# <span data-ttu-id="9e1cc-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9e1cc-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="9e1cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e1cc-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1cc-103">Kullanıcı ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-103">Sets user details.</span></span>

## <span data-ttu-id="9e1cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e1cc-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e1cc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e1cc-105">DESCRIPTION</span></span>
<span data-ttu-id="9e1cc-106">**Set-Azapsananagementuser** cmdlet 'i Kullanıcı ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="9e1cc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e1cc-107">EXAMPLES</span></span>

### <span data-ttu-id="9e1cc-108">Örnek 1: kullanıcının parolasını, e-posta adresini ve durumunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="9e1cc-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="9e1cc-109">Bu komut yeni bir Kullanıcı parolası ve e-posta adresi ayarlar ve kullanıcıyı engeller.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="9e1cc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e1cc-110">PARAMETERS</span></span>

### <span data-ttu-id="9e1cc-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9e1cc-111">-Context</span></span>
<span data-ttu-id="9e1cc-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="9e1cc-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-113">This parameter is required.</span></span>

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

### <span data-ttu-id="9e1cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1cc-114">-DefaultProfile</span></span>
<span data-ttu-id="9e1cc-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e1cc-116">-E-posta</span><span class="sxs-lookup"><span data-stu-id="9e1cc-116">-Email</span></span>
<span data-ttu-id="9e1cc-117">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="9e1cc-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="9e1cc-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e1cc-119">-FirstName</span></span>
<span data-ttu-id="9e1cc-120">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="9e1cc-121">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="9e1cc-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="9e1cc-122">-LastName</span></span>
<span data-ttu-id="9e1cc-123">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="9e1cc-124">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="9e1cc-125">Not</span><span class="sxs-lookup"><span data-stu-id="9e1cc-125">-Note</span></span>
<span data-ttu-id="9e1cc-126">Kullanıcı hakkında bir Not belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-126">Specifies a note about the user.</span></span>
<span data-ttu-id="9e1cc-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-127">This parameter is optional.</span></span>
<span data-ttu-id="9e1cc-128">Bu parametrenin varsayılan değeri $null.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="9e1cc-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9e1cc-129">-PassThru</span></span>
<span data-ttu-id="9e1cc-130">geçiş</span><span class="sxs-lookup"><span data-stu-id="9e1cc-130">passthru</span></span>

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

### <span data-ttu-id="9e1cc-131">-Parola</span><span class="sxs-lookup"><span data-stu-id="9e1cc-131">-Password</span></span>
<span data-ttu-id="9e1cc-132">Kullanıcı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-132">Specifies the user password.</span></span>
<span data-ttu-id="9e1cc-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="9e1cc-134">Durumlu</span><span class="sxs-lookup"><span data-stu-id="9e1cc-134">-State</span></span>
<span data-ttu-id="9e1cc-135">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-135">Specifies the user state.</span></span>
<span data-ttu-id="9e1cc-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-136">This parameter is optional.</span></span>
<span data-ttu-id="9e1cc-137">Varsayılan değer etkindir.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-137">The default value is Active.</span></span>

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

### <span data-ttu-id="9e1cc-138">-UserID</span><span class="sxs-lookup"><span data-stu-id="9e1cc-138">-UserId</span></span>
<span data-ttu-id="9e1cc-139">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-139">Specifies the user ID.</span></span>
<span data-ttu-id="9e1cc-140">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-140">This parameter is required.</span></span>

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

### <span data-ttu-id="9e1cc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1cc-141">CommonParameters</span></span>
<span data-ttu-id="9e1cc-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e1cc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1cc-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e1cc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1cc-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e1cc-144">INPUTS</span></span>

### <span data-ttu-id="9e1cc-145">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="9e1cc-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e1cc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9e1cc-146">System.String</span></span>

### <span data-ttu-id="9e1cc-147">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="9e1cc-147">System.Security.SecureString</span></span>

### <span data-ttu-id="9e1cc-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuserstate</span><span class="sxs-lookup"><span data-stu-id="9e1cc-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="9e1cc-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9e1cc-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9e1cc-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e1cc-150">OUTPUTS</span></span>

### <span data-ttu-id="9e1cc-151">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="9e1cc-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="9e1cc-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e1cc-152">NOTES</span></span>

## <span data-ttu-id="9e1cc-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e1cc-153">RELATED LINKS</span></span>

[<span data-ttu-id="9e1cc-154">Get-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="9e1cc-154">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="9e1cc-155">Yeni-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="9e1cc-155">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="9e1cc-156">Remove-Azapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="9e1cc-156">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


