---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: a9d36dca9894a10c76f2ca5a96880f4aafecb5e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587013"
---
# <span data-ttu-id="87fc1-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="87fc1-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="87fc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="87fc1-103">Kullanıcı ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="87fc1-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87fc1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87fc1-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <String>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87fc1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="87fc1-105">DESCRIPTION</span></span>
<span data-ttu-id="87fc1-106">**Set-Azurermapsananagementuser** cmdlet 'i Kullanıcı ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="87fc1-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="87fc1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87fc1-107">EXAMPLES</span></span>

### <span data-ttu-id="87fc1-108">Örnek 1: kullanıcının parolasını, e-posta adresini ve durumunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="87fc1-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password "asdfgh" -State "Blocked"
```

<span data-ttu-id="87fc1-109">Bu komut yeni bir Kullanıcı parolası ve e-posta adresi ayarlar ve kullanıcıyı engeller.</span><span class="sxs-lookup"><span data-stu-id="87fc1-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="87fc1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87fc1-110">PARAMETERS</span></span>

### <span data-ttu-id="87fc1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="87fc1-111">-Context</span></span>
<span data-ttu-id="87fc1-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87fc1-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="87fc1-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="87fc1-113">This parameter is required.</span></span>

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

### <span data-ttu-id="87fc1-114">-E-posta</span><span class="sxs-lookup"><span data-stu-id="87fc1-114">-Email</span></span>
<span data-ttu-id="87fc1-115">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87fc1-115">Specifies the email address of the user.</span></span>
<span data-ttu-id="87fc1-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="87fc1-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="87fc1-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="87fc1-117">-FirstName</span></span>
<span data-ttu-id="87fc1-118">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87fc1-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="87fc1-119">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="87fc1-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="87fc1-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="87fc1-120">-LastName</span></span>
<span data-ttu-id="87fc1-121">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87fc1-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="87fc1-122">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="87fc1-122">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="87fc1-123">Not</span><span class="sxs-lookup"><span data-stu-id="87fc1-123">-Note</span></span>
<span data-ttu-id="87fc1-124">Kullanıcı hakkında bir Not belirtir.</span><span class="sxs-lookup"><span data-stu-id="87fc1-124">Specifies a note about the user.</span></span>
<span data-ttu-id="87fc1-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="87fc1-125">This parameter is optional.</span></span>
<span data-ttu-id="87fc1-126">Bu parametrenin varsayılan değeri $null.</span><span class="sxs-lookup"><span data-stu-id="87fc1-126">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="87fc1-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="87fc1-127">-PassThru</span></span>
<span data-ttu-id="87fc1-128">geçiş</span><span class="sxs-lookup"><span data-stu-id="87fc1-128">passthru</span></span>

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

### <span data-ttu-id="87fc1-129">-Parola</span><span class="sxs-lookup"><span data-stu-id="87fc1-129">-Password</span></span>
<span data-ttu-id="87fc1-130">Kullanıcı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87fc1-130">Specifies the user password.</span></span>
<span data-ttu-id="87fc1-131">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="87fc1-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="87fc1-132">Durumlu</span><span class="sxs-lookup"><span data-stu-id="87fc1-132">-State</span></span>
<span data-ttu-id="87fc1-133">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87fc1-133">Specifies the user state.</span></span>
<span data-ttu-id="87fc1-134">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="87fc1-134">This parameter is optional.</span></span>
<span data-ttu-id="87fc1-135">Varsayılan değer etkindir.</span><span class="sxs-lookup"><span data-stu-id="87fc1-135">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87fc1-136">-UserID</span><span class="sxs-lookup"><span data-stu-id="87fc1-136">-UserId</span></span>
<span data-ttu-id="87fc1-137">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="87fc1-137">Specifies the user ID.</span></span>
<span data-ttu-id="87fc1-138">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="87fc1-138">This parameter is required.</span></span>

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

### <span data-ttu-id="87fc1-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87fc1-139">-DefaultProfile</span></span>
<span data-ttu-id="87fc1-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87fc1-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87fc1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87fc1-141">CommonParameters</span></span>
<span data-ttu-id="87fc1-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87fc1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87fc1-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87fc1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87fc1-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87fc1-144">INPUTS</span></span>

## <span data-ttu-id="87fc1-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87fc1-145">OUTPUTS</span></span>

### <span data-ttu-id="87fc1-146">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="87fc1-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="87fc1-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87fc1-147">NOTES</span></span>

## <span data-ttu-id="87fc1-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87fc1-148">RELATED LINKS</span></span>

[<span data-ttu-id="87fc1-149">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="87fc1-149">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="87fc1-150">Yeni-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="87fc1-150">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="87fc1-151">Remove-Azurermapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="87fc1-151">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


