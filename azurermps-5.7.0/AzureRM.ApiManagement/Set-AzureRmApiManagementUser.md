---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: d3825b4887d2361a4bb378bfddc3085773efd84b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594149"
---
# <span data-ttu-id="0c6c9-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0c6c9-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="0c6c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c6c9-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6c9-103">Kullanıcı ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c6c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c6c9-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c6c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c6c9-105">DESCRIPTION</span></span>
<span data-ttu-id="0c6c9-106">**Set-Azurermapsananagementuser** cmdlet 'i Kullanıcı ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="0c6c9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c6c9-107">EXAMPLES</span></span>

### <span data-ttu-id="0c6c9-108">Örnek 1: kullanıcının parolasını, e-posta adresini ve durumunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="0c6c9-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="0c6c9-109">Bu komut yeni bir Kullanıcı parolası ve e-posta adresi ayarlar ve kullanıcıyı engeller.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="0c6c9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c6c9-110">PARAMETERS</span></span>

### <span data-ttu-id="0c6c9-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0c6c9-111">-Context</span></span>
<span data-ttu-id="0c6c9-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0c6c9-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-113">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6c9-114">-DefaultProfile</span></span>
<span data-ttu-id="0c6c9-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c9-116">-E-posta</span><span class="sxs-lookup"><span data-stu-id="0c6c9-116">-Email</span></span>
<span data-ttu-id="0c6c9-117">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="0c6c9-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-118">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c6c9-119">-FirstName</span></span>
<span data-ttu-id="0c6c9-120">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="0c6c9-121">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-121">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c9-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="0c6c9-122">-LastName</span></span>
<span data-ttu-id="0c6c9-123">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="0c6c9-124">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-124">This parameter is must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c9-125">Not</span><span class="sxs-lookup"><span data-stu-id="0c6c9-125">-Note</span></span>
<span data-ttu-id="0c6c9-126">Kullanıcı hakkında bir Not belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-126">Specifies a note about the user.</span></span>
<span data-ttu-id="0c6c9-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-127">This parameter is optional.</span></span>
<span data-ttu-id="0c6c9-128">Bu parametrenin varsayılan değeri $null.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-128">The default value of this parameter is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c9-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0c6c9-129">-PassThru</span></span>
<span data-ttu-id="0c6c9-130">geçiş</span><span class="sxs-lookup"><span data-stu-id="0c6c9-130">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c9-131">-Parola</span><span class="sxs-lookup"><span data-stu-id="0c6c9-131">-Password</span></span>
<span data-ttu-id="0c6c9-132">Kullanıcı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-132">Specifies the user password.</span></span>
<span data-ttu-id="0c6c9-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-133">This parameter is optional.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c9-134">Durumlu</span><span class="sxs-lookup"><span data-stu-id="0c6c9-134">-State</span></span>
<span data-ttu-id="0c6c9-135">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-135">Specifies the user state.</span></span>
<span data-ttu-id="0c6c9-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-136">This parameter is optional.</span></span>
<span data-ttu-id="0c6c9-137">Varsayılan değer etkindir.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-137">The default value is Active.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c9-138">-UserID</span><span class="sxs-lookup"><span data-stu-id="0c6c9-138">-UserId</span></span>
<span data-ttu-id="0c6c9-139">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-139">Specifies the user ID.</span></span>
<span data-ttu-id="0c6c9-140">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-140">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6c9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6c9-141">CommonParameters</span></span>
<span data-ttu-id="0c6c9-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6c9-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c6c9-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6c9-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c6c9-144">INPUTS</span></span>

### <span data-ttu-id="0c6c9-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0c6c9-145">None</span></span>
<span data-ttu-id="0c6c9-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0c6c9-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0c6c9-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c6c9-147">OUTPUTS</span></span>

### <span data-ttu-id="0c6c9-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="0c6c9-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="0c6c9-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c6c9-149">NOTES</span></span>

## <span data-ttu-id="0c6c9-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c6c9-150">RELATED LINKS</span></span>

[<span data-ttu-id="0c6c9-151">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="0c6c9-151">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="0c6c9-152">Yeni-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="0c6c9-152">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="0c6c9-153">Remove-Azurermapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="0c6c9-153">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


