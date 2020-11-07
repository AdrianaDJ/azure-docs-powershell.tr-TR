---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 885d552f6040d4c88c007a37f839ac030ba671c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751145"
---
# <span data-ttu-id="8768e-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8768e-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="8768e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8768e-102">SYNOPSIS</span></span>
<span data-ttu-id="8768e-103">Abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="8768e-103">Gets subscriptions.</span></span>

## <span data-ttu-id="8768e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8768e-104">SYNTAX</span></span>

### <span data-ttu-id="8768e-105">Getallabonelikleri (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8768e-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8768e-106">Getbysubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="8768e-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8768e-107">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="8768e-107">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8768e-108">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="8768e-108">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8768e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="8768e-109">DESCRIPTION</span></span>
<span data-ttu-id="8768e-110">**Get-Azapsananagementsubscription** cmdlet 'i belirtilen bir aboneliği veya herhangi bir abonelik belirtilmemişse tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="8768e-110">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="8768e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8768e-111">EXAMPLES</span></span>

### <span data-ttu-id="8768e-112">Örnek 1: tüm abonelikleri al</span><span class="sxs-lookup"><span data-stu-id="8768e-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="8768e-113">Bu komut tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="8768e-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="8768e-114">Örnek 2: belirtilen KIMLIĞE sahip bir abonelik alın</span><span class="sxs-lookup"><span data-stu-id="8768e-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="8768e-115">Bu komut, KIMLIĞI bir abonelik alır.</span><span class="sxs-lookup"><span data-stu-id="8768e-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="8768e-116">Örnek 3: kullanıcıya yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="8768e-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="8768e-117">Bu komut kullanıcının aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="8768e-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="8768e-118">Örnek 4: bir ürüne yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="8768e-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="8768e-119">Bu komut, ürünün tüm aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="8768e-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="8768e-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8768e-120">PARAMETERS</span></span>

### <span data-ttu-id="8768e-121">-Context</span><span class="sxs-lookup"><span data-stu-id="8768e-121">-Context</span></span>
<span data-ttu-id="8768e-122">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8768e-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8768e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8768e-123">-DefaultProfile</span></span>
<span data-ttu-id="8768e-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8768e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8768e-125">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="8768e-125">-ProductId</span></span>
<span data-ttu-id="8768e-126">Ürün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8768e-126">Specifies a product identifier.</span></span>
<span data-ttu-id="8768e-127">Belirtilmişse, bu cmdlet ürün tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="8768e-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8768e-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="8768e-128">-SubscriptionId</span></span>
<span data-ttu-id="8768e-129">Abonelik tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8768e-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="8768e-130">Belirtilmişse, bu cmdlet tanımlayıcının tanımlayıcısını bulur.</span><span class="sxs-lookup"><span data-stu-id="8768e-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8768e-131">-UserID</span><span class="sxs-lookup"><span data-stu-id="8768e-131">-UserId</span></span>
<span data-ttu-id="8768e-132">Kullanıcı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8768e-132">Specifies a user identifier.</span></span>
<span data-ttu-id="8768e-133">Belirtilmişse, bu cmdlet Kullanıcı tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="8768e-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8768e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8768e-134">CommonParameters</span></span>
<span data-ttu-id="8768e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8768e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8768e-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8768e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8768e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8768e-137">INPUTS</span></span>

### <span data-ttu-id="8768e-138">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="8768e-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8768e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8768e-139">System.String</span></span>

## <span data-ttu-id="8768e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8768e-140">OUTPUTS</span></span>

### <span data-ttu-id="8768e-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="8768e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="8768e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8768e-142">NOTES</span></span>

## <span data-ttu-id="8768e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8768e-143">RELATED LINKS</span></span>

[<span data-ttu-id="8768e-144">Yeni-Azsız abonelik</span><span class="sxs-lookup"><span data-stu-id="8768e-144">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="8768e-145">Remove-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="8768e-145">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="8768e-146">Set-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="8768e-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


