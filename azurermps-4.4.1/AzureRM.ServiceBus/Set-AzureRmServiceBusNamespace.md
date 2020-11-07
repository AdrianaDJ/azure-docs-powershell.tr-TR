---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 134e0d20566a8310a381a38297984202b7509250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764518"
---
# <span data-ttu-id="97167-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="97167-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="97167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97167-102">SYNOPSIS</span></span>
<span data-ttu-id="97167-103">Var olan bir hizmet veri yolu ad alanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="97167-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97167-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97167-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> -Name <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97167-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97167-105">DESCRIPTION</span></span>
<span data-ttu-id="97167-106">**Set-AzureRmServiceBusNamespace** cmdlet 'i, kaynak grubunda belirtilen hizmet veri yolu ad alanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="97167-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="97167-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97167-107">EXAMPLES</span></span>

### <span data-ttu-id="97167-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="97167-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 10 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 10 , Tier : Standard
ProvisioningState  : Succeeded
Status             :
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
Enabled            : False
```

<span data-ttu-id="97167-109">Hizmet veri yolu ad alanını yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="97167-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="97167-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97167-110">PARAMETERS</span></span>

### <span data-ttu-id="97167-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="97167-111">-Location</span></span>
<span data-ttu-id="97167-112">Hizmet veri yolu ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="97167-112">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="97167-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97167-113">-ResourceGroupName</span></span>
<span data-ttu-id="97167-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="97167-114">The resource group name.</span></span>

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

### <span data-ttu-id="97167-115">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="97167-115">-SkuCapacity</span></span>
<span data-ttu-id="97167-116">Ad alanı SKU kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="97167-116">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="97167-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="97167-117">-SkuName</span></span>
<span data-ttu-id="97167-118">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="97167-118">The namespace SKU name.</span></span>

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

### <span data-ttu-id="97167-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="97167-119">-Tag</span></span>
<span data-ttu-id="97167-120">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="97167-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="97167-121">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="97167-121">For example:</span></span>

<span data-ttu-id="97167-122">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="97167-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="97167-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="97167-123">-Confirm</span></span>
<span data-ttu-id="97167-124">Hizmet veri yolu ad alanını belirtilen bilgilerle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="97167-124">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="97167-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97167-125">-WhatIf</span></span>
<span data-ttu-id="97167-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97167-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97167-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97167-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97167-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97167-128">-DefaultProfile</span></span>
<span data-ttu-id="97167-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97167-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97167-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="97167-130">-Name</span></span>
<span data-ttu-id="97167-131">ServiceBus ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="97167-131">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97167-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97167-132">CommonParameters</span></span>
<span data-ttu-id="97167-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97167-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97167-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97167-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97167-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97167-135">INPUTS</span></span>

### <span data-ttu-id="97167-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="97167-136">-ResourceGroup</span></span>
 <span data-ttu-id="97167-137">System. String</span><span class="sxs-lookup"><span data-stu-id="97167-137">System.String</span></span>

### <span data-ttu-id="97167-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="97167-138">-NamespaceName</span></span>
 <span data-ttu-id="97167-139">System. String</span><span class="sxs-lookup"><span data-stu-id="97167-139">System.String</span></span>

### <span data-ttu-id="97167-140">-Konum</span><span class="sxs-lookup"><span data-stu-id="97167-140">-Location</span></span>
 <span data-ttu-id="97167-141">System. String</span><span class="sxs-lookup"><span data-stu-id="97167-141">System.String</span></span>

### <span data-ttu-id="97167-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="97167-142">-SkuName</span></span>
 <span data-ttu-id="97167-143">System. String</span><span class="sxs-lookup"><span data-stu-id="97167-143">System.String</span></span>

### <span data-ttu-id="97167-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="97167-144">-Tag</span></span>
 <span data-ttu-id="97167-145">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="97167-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="97167-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97167-146">OUTPUTS</span></span>

### <span data-ttu-id="97167-147">Microsoft. Azure. Commands. ServiceBus. modeller. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="97167-147">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="97167-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97167-148">NOTES</span></span>
## <span data-ttu-id="97167-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97167-149">RELATED LINKS</span></span>

## <span data-ttu-id="97167-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97167-150">RELATED LINKS</span></span>

