---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: fa7b44710aa51a138729d9a04a41a82ec2769f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765129"
---
# <span data-ttu-id="85d6f-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="85d6f-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="85d6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="85d6f-103">Yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="85d6f-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85d6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85d6f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85d6f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="85d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="85d6f-106">**Yeni-Azurermapsananagementuser** cmdlet 'i yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="85d6f-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="85d6f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85d6f-107">EXAMPLES</span></span>

### <span data-ttu-id="85d6f-108">Örnek 1: yeni bir kullanıcıyı kaydettirme</span><span class="sxs-lookup"><span data-stu-id="85d6f-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="85d6f-109">Bu komut, Patti Fuller adlı yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="85d6f-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="85d6f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85d6f-110">PARAMETERS</span></span>

### <span data-ttu-id="85d6f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="85d6f-111">-Context</span></span>
<span data-ttu-id="85d6f-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85d6f-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="85d6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d6f-113">-DefaultProfile</span></span>
<span data-ttu-id="85d6f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="85d6f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="85d6f-115">-E-posta</span><span class="sxs-lookup"><span data-stu-id="85d6f-115">-Email</span></span>
<span data-ttu-id="85d6f-116">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85d6f-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="85d6f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="85d6f-117">-FirstName</span></span>
<span data-ttu-id="85d6f-118">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85d6f-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="85d6f-119">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="85d6f-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="85d6f-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="85d6f-120">-LastName</span></span>
<span data-ttu-id="85d6f-121">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85d6f-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="85d6f-122">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="85d6f-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="85d6f-123">Not</span><span class="sxs-lookup"><span data-stu-id="85d6f-123">-Note</span></span>
<span data-ttu-id="85d6f-124">Kullanıcı hakkında bir Not belirtir.</span><span class="sxs-lookup"><span data-stu-id="85d6f-124">Specifies a note about the user.</span></span>
<span data-ttu-id="85d6f-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="85d6f-125">This parameter is optional.</span></span>
<span data-ttu-id="85d6f-126">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="85d6f-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="85d6f-127">-Parola</span><span class="sxs-lookup"><span data-stu-id="85d6f-127">-Password</span></span>
<span data-ttu-id="85d6f-128">Kullanıcı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85d6f-128">Specifies the user password.</span></span>
<span data-ttu-id="85d6f-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="85d6f-129">This parameter is required.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d6f-130">Durumlu</span><span class="sxs-lookup"><span data-stu-id="85d6f-130">-State</span></span>
<span data-ttu-id="85d6f-131">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="85d6f-131">Specifies the user state.</span></span>
<span data-ttu-id="85d6f-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="85d6f-132">This parameter is optional.</span></span>
<span data-ttu-id="85d6f-133">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="85d6f-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="85d6f-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="85d6f-134">-UserId</span></span>
<span data-ttu-id="85d6f-135">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="85d6f-135">Specifies the user ID.</span></span>
<span data-ttu-id="85d6f-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="85d6f-136">This parameter is optional.</span></span>
<span data-ttu-id="85d6f-137">Bu parametre belirtilmezse, bu cmdlet bir kullanıcı KIMLIĞI oluşturur.</span><span class="sxs-lookup"><span data-stu-id="85d6f-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="85d6f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d6f-138">CommonParameters</span></span>
<span data-ttu-id="85d6f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85d6f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d6f-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85d6f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d6f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85d6f-141">INPUTS</span></span>

### <span data-ttu-id="85d6f-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="85d6f-142">None</span></span>
<span data-ttu-id="85d6f-143">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="85d6f-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85d6f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85d6f-144">OUTPUTS</span></span>

### <span data-ttu-id="85d6f-145">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="85d6f-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="85d6f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85d6f-146">NOTES</span></span>

## <span data-ttu-id="85d6f-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85d6f-147">RELATED LINKS</span></span>

[<span data-ttu-id="85d6f-148">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="85d6f-148">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="85d6f-149">Set-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="85d6f-149">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


