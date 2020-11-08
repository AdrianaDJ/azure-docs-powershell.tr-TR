---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273961"
---
# <span data-ttu-id="01af9-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="01af9-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="01af9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01af9-102">SYNOPSIS</span></span>
<span data-ttu-id="01af9-103">Var olan bir hizmet veri yolu ad alanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="01af9-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="01af9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01af9-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01af9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01af9-105">DESCRIPTION</span></span>
<span data-ttu-id="01af9-106">**Set-AzServiceBusNamespace** cmdlet 'i, kaynak grubunda belirtilen hizmet veri yolu ad alanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="01af9-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="01af9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01af9-107">EXAMPLES</span></span>

### <span data-ttu-id="01af9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="01af9-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="01af9-109">Hizmet veri yolu ad alanını yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="01af9-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="01af9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01af9-110">PARAMETERS</span></span>

### <span data-ttu-id="01af9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01af9-111">-DefaultProfile</span></span>
<span data-ttu-id="01af9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01af9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01af9-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="01af9-113">-Location</span></span>
<span data-ttu-id="01af9-114">Hizmet veri yolu ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="01af9-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="01af9-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="01af9-115">-Name</span></span>
<span data-ttu-id="01af9-116">ServiceBus ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="01af9-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="01af9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01af9-117">-ResourceGroupName</span></span>
<span data-ttu-id="01af9-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="01af9-118">The resource group name.</span></span>

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

### <span data-ttu-id="01af9-119">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="01af9-119">-SkuCapacity</span></span>
<span data-ttu-id="01af9-120">Ad alanı SKU kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="01af9-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="01af9-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="01af9-121">-SkuName</span></span>
<span data-ttu-id="01af9-122">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="01af9-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="01af9-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="01af9-123">-Tag</span></span>
<span data-ttu-id="01af9-124">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="01af9-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="01af9-125">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="01af9-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="01af9-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="01af9-126">-Confirm</span></span>
<span data-ttu-id="01af9-127">Hizmet veri yolu ad alanını belirtilen bilgilerle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="01af9-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="01af9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01af9-128">-WhatIf</span></span>
<span data-ttu-id="01af9-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01af9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01af9-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01af9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01af9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01af9-131">CommonParameters</span></span>
<span data-ttu-id="01af9-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01af9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01af9-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01af9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01af9-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01af9-134">INPUTS</span></span>

### <span data-ttu-id="01af9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="01af9-135">System.String</span></span>

### <span data-ttu-id="01af9-136">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="01af9-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="01af9-137">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="01af9-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="01af9-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01af9-138">OUTPUTS</span></span>

### <span data-ttu-id="01af9-139">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="01af9-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="01af9-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01af9-140">NOTES</span></span>

## <span data-ttu-id="01af9-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01af9-141">RELATED LINKS</span></span>
