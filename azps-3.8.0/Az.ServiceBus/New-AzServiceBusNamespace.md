---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103718"
---
# <span data-ttu-id="db134-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="db134-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="db134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db134-102">SYNOPSIS</span></span>
<span data-ttu-id="db134-103">Yeni bir hizmet veri yolu ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db134-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="db134-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db134-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db134-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db134-105">DESCRIPTION</span></span>
<span data-ttu-id="db134-106">**New-AzServiceBusNamespace** cmdlet 'i, yeni bir Service Bus ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db134-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="db134-107">Oluşturulduktan sonra, ad alanı kaynak bildirimi sabittir.</span><span class="sxs-lookup"><span data-stu-id="db134-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="db134-108">Bu işlem idempotent.</span><span class="sxs-lookup"><span data-stu-id="db134-108">This operation is idempotent.</span></span>

## <span data-ttu-id="db134-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db134-109">EXAMPLES</span></span>

### <span data-ttu-id="db134-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="db134-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="db134-111">Belirtilen kaynak grubunda yeni bir hizmet veri yolu ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db134-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="db134-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db134-112">PARAMETERS</span></span>

### <span data-ttu-id="db134-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db134-113">-DefaultProfile</span></span>
<span data-ttu-id="db134-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db134-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db134-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="db134-115">-Location</span></span>
<span data-ttu-id="db134-116">Hizmet veri yolu ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="db134-116">The Service Bus namespace location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db134-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="db134-117">-Name</span></span>
<span data-ttu-id="db134-118">ServiceBus ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="db134-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db134-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db134-119">-ResourceGroupName</span></span>
<span data-ttu-id="db134-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="db134-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db134-121">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="db134-121">-SkuCapacity</span></span>
<span data-ttu-id="db134-122">Hizmet veri yolu Premium ad alanı üretilen iş birimleri, izin verilen değerler 1 veya 2 veya 4</span><span class="sxs-lookup"><span data-stu-id="db134-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db134-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="db134-123">-SkuName</span></span>
<span data-ttu-id="db134-124">Hizmet veri yolu ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="db134-124">The Service Bus namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db134-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="db134-125">-Tag</span></span>
<span data-ttu-id="db134-126">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="db134-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="db134-127">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="db134-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db134-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="db134-128">-Confirm</span></span>
<span data-ttu-id="db134-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db134-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db134-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db134-130">-WhatIf</span></span>
<span data-ttu-id="db134-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db134-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db134-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db134-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db134-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db134-133">CommonParameters</span></span>
<span data-ttu-id="db134-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db134-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db134-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db134-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db134-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db134-136">INPUTS</span></span>

### <span data-ttu-id="db134-137">System. String</span><span class="sxs-lookup"><span data-stu-id="db134-137">System.String</span></span>

### <span data-ttu-id="db134-138">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="db134-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="db134-139">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="db134-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="db134-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db134-140">OUTPUTS</span></span>

### <span data-ttu-id="db134-141">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="db134-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="db134-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db134-142">NOTES</span></span>

## <span data-ttu-id="db134-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db134-143">RELATED LINKS</span></span>
