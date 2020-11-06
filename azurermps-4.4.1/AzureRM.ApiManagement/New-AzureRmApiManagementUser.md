---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 93e6ce5a96afd1c3b297d6296c3491445593d430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591839"
---
# <span data-ttu-id="67d55-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="67d55-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="67d55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d55-102">SYNOPSIS</span></span>
<span data-ttu-id="67d55-103">Yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="67d55-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67d55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67d55-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <String> [-State <PsApiManagementUserState>] [-Note <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67d55-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67d55-105">DESCRIPTION</span></span>
<span data-ttu-id="67d55-106">**Yeni-Azurermapsananagementuser** cmdlet 'i yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="67d55-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="67d55-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67d55-107">EXAMPLES</span></span>

### <span data-ttu-id="67d55-108">Örnek 1: yeni bir kullanıcıyı kaydettirme</span><span class="sxs-lookup"><span data-stu-id="67d55-108">Example 1: Register a new user</span></span>
```
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password "qwerty"
```

<span data-ttu-id="67d55-109">Bu komut, Patti Fuller adlı yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="67d55-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="67d55-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67d55-110">PARAMETERS</span></span>

### <span data-ttu-id="67d55-111">-Context</span><span class="sxs-lookup"><span data-stu-id="67d55-111">-Context</span></span>
<span data-ttu-id="67d55-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d55-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="67d55-113">-E-posta</span><span class="sxs-lookup"><span data-stu-id="67d55-113">-Email</span></span>
<span data-ttu-id="67d55-114">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d55-114">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="67d55-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="67d55-115">-FirstName</span></span>
<span data-ttu-id="67d55-116">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d55-116">Specifies the first name of the user.</span></span>
<span data-ttu-id="67d55-117">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="67d55-117">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="67d55-118">-LastName</span><span class="sxs-lookup"><span data-stu-id="67d55-118">-LastName</span></span>
<span data-ttu-id="67d55-119">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d55-119">Specifies the last name of the user.</span></span>
<span data-ttu-id="67d55-120">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="67d55-120">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="67d55-121">Not</span><span class="sxs-lookup"><span data-stu-id="67d55-121">-Note</span></span>
<span data-ttu-id="67d55-122">Kullanıcı hakkında bir Not belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d55-122">Specifies a note about the user.</span></span>
<span data-ttu-id="67d55-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="67d55-123">This parameter is optional.</span></span>
<span data-ttu-id="67d55-124">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="67d55-124">The default value is $Null.</span></span>

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

### <span data-ttu-id="67d55-125">-Parola</span><span class="sxs-lookup"><span data-stu-id="67d55-125">-Password</span></span>
<span data-ttu-id="67d55-126">Kullanıcı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d55-126">Specifies the user password.</span></span>
<span data-ttu-id="67d55-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="67d55-127">This parameter is required.</span></span>

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

### <span data-ttu-id="67d55-128">Durumlu</span><span class="sxs-lookup"><span data-stu-id="67d55-128">-State</span></span>
<span data-ttu-id="67d55-129">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d55-129">Specifies the user state.</span></span>
<span data-ttu-id="67d55-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="67d55-130">This parameter is optional.</span></span>
<span data-ttu-id="67d55-131">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="67d55-131">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d55-132">-UserID</span><span class="sxs-lookup"><span data-stu-id="67d55-132">-UserId</span></span>
<span data-ttu-id="67d55-133">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="67d55-133">Specifies the user ID.</span></span>
<span data-ttu-id="67d55-134">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="67d55-134">This parameter is optional.</span></span>
<span data-ttu-id="67d55-135">Bu parametre belirtilmezse, bu cmdlet bir kullanıcı KIMLIĞI oluşturur.</span><span class="sxs-lookup"><span data-stu-id="67d55-135">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="67d55-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d55-136">-DefaultProfile</span></span>
<span data-ttu-id="67d55-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67d55-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67d55-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d55-138">CommonParameters</span></span>
<span data-ttu-id="67d55-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67d55-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d55-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67d55-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d55-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67d55-141">INPUTS</span></span>

## <span data-ttu-id="67d55-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67d55-142">OUTPUTS</span></span>

### <span data-ttu-id="67d55-143">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="67d55-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="67d55-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67d55-144">NOTES</span></span>

## <span data-ttu-id="67d55-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67d55-145">RELATED LINKS</span></span>

[<span data-ttu-id="67d55-146">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="67d55-146">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="67d55-147">Set-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="67d55-147">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


