---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 6ac46fc8b8f94480e11f00d44efc690d97ee56a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763797"
---
# <span data-ttu-id="02b64-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="02b64-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="02b64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02b64-102">SYNOPSIS</span></span>
<span data-ttu-id="02b64-103">Var olan bir hizmet veri yolu ad alanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="02b64-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02b64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02b64-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02b64-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="02b64-105">DESCRIPTION</span></span>
<span data-ttu-id="02b64-106">**Set-AzureRmServiceBusNamespace** cmdlet 'i, kaynak grubunda belirtilen hizmet veri yolu ad alanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="02b64-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="02b64-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02b64-107">EXAMPLES</span></span>

### <span data-ttu-id="02b64-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02b64-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="02b64-109">Hizmet veri yolu ad alanını yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="02b64-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="02b64-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02b64-110">PARAMETERS</span></span>

### <span data-ttu-id="02b64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02b64-111">-DefaultProfile</span></span>
<span data-ttu-id="02b64-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02b64-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02b64-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="02b64-113">-Location</span></span>
<span data-ttu-id="02b64-114">Hizmet veri yolu ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="02b64-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="02b64-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="02b64-115">-Name</span></span>
<span data-ttu-id="02b64-116">ServiceBus ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="02b64-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="02b64-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02b64-117">-ResourceGroupName</span></span>
<span data-ttu-id="02b64-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="02b64-118">The resource group name.</span></span>

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

### <span data-ttu-id="02b64-119">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="02b64-119">-SkuCapacity</span></span>
<span data-ttu-id="02b64-120">Ad alanı SKU kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="02b64-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="02b64-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="02b64-121">-SkuName</span></span>
<span data-ttu-id="02b64-122">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="02b64-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="02b64-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="02b64-123">-Tag</span></span>
<span data-ttu-id="02b64-124">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="02b64-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="02b64-125">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="02b64-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="02b64-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="02b64-126">-Confirm</span></span>
<span data-ttu-id="02b64-127">Hizmet veri yolu ad alanını belirtilen bilgilerle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="02b64-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="02b64-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02b64-128">-WhatIf</span></span>
<span data-ttu-id="02b64-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02b64-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02b64-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02b64-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02b64-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b64-131">CommonParameters</span></span>
<span data-ttu-id="02b64-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02b64-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b64-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02b64-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b64-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02b64-134">INPUTS</span></span>

### <span data-ttu-id="02b64-135">System. String</span><span class="sxs-lookup"><span data-stu-id="02b64-135">System.String</span></span>

### <span data-ttu-id="02b64-136">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="02b64-136">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="02b64-137">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="02b64-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="02b64-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02b64-138">OUTPUTS</span></span>

### <span data-ttu-id="02b64-139">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="02b64-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="02b64-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02b64-140">NOTES</span></span>

## <span data-ttu-id="02b64-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02b64-141">RELATED LINKS</span></span>
