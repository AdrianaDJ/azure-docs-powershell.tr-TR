---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6fd3f000f7c91f0475cd18802dd6a9d096d35f5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591956"
---
# <span data-ttu-id="dcc32-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="dcc32-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="dcc32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcc32-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc32-103">Belirtilen olay hub ad boşluğunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dcc32-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcc32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcc32-104">SYNTAX</span></span>

### <span data-ttu-id="dcc32-105">NamespaceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dcc32-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcc32-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc32-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcc32-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcc32-107">DESCRIPTION</span></span>
<span data-ttu-id="dcc32-108">Set-AzureRmEventHubNamespace cmdlet 'i belirtilen olay hub 'Larının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dcc32-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="dcc32-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcc32-109">EXAMPLES</span></span>

### <span data-ttu-id="dcc32-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dcc32-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="dcc32-111">\`Mynamespacename ad alanının durumunu \` oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="dcc32-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="dcc32-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dcc32-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="dcc32-113">\` \` Autoinir = Enabled ve MaximumThroughputUnits = 10 olan mynamespacename 'in durumunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="dcc32-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="dcc32-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcc32-114">PARAMETERS</span></span>

### <span data-ttu-id="dcc32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc32-115">-DefaultProfile</span></span>
<span data-ttu-id="dcc32-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcc32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcc32-117">-Enableautoinir</span><span class="sxs-lookup"><span data-stu-id="dcc32-117">-EnableAutoInflate</span></span>
<span data-ttu-id="dcc32-118">Autoinir özelliğinin etkinleştirilip etkinleştirilmediğini gösterir</span><span class="sxs-lookup"><span data-stu-id="dcc32-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc32-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="dcc32-119">-Location</span></span>
<span data-ttu-id="dcc32-120">EventHub ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="dcc32-120">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc32-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="dcc32-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="dcc32-122">Üretilen iş birimlerinin üst limiti otomatik değer değeri etkinleştirildiğinde, değer 0-20 üretilen iş birimi cinsinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dcc32-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc32-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="dcc32-123">-Name</span></span>
<span data-ttu-id="dcc32-124">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="dcc32-124">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc32-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcc32-125">-ResourceGroupName</span></span>
<span data-ttu-id="dcc32-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dcc32-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc32-127">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="dcc32-127">-SkuCapacity</span></span>
<span data-ttu-id="dcc32-128">Eventhub üretim birimleri.</span><span class="sxs-lookup"><span data-stu-id="dcc32-128">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc32-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dcc32-129">-SkuName</span></span>
<span data-ttu-id="dcc32-130">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="dcc32-130">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc32-131">Durumlu</span><span class="sxs-lookup"><span data-stu-id="dcc32-131">-State</span></span>
<span data-ttu-id="dcc32-132">Ad alanını devre dışı bırakma/etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="dcc32-132">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc32-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dcc32-133">-Tag</span></span>
<span data-ttu-id="dcc32-134">Kaynak etiketini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="dcc32-134">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc32-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="dcc32-135">-Confirm</span></span>
<span data-ttu-id="dcc32-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dcc32-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc32-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcc32-137">-WhatIf</span></span>
<span data-ttu-id="dcc32-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dcc32-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcc32-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dcc32-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc32-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc32-140">CommonParameters</span></span>
<span data-ttu-id="dcc32-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcc32-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc32-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcc32-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc32-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcc32-143">INPUTS</span></span>

### <span data-ttu-id="dcc32-144">System. String</span><span class="sxs-lookup"><span data-stu-id="dcc32-144">System.String</span></span>

### <span data-ttu-id="dcc32-145">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="dcc32-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="dcc32-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. modeller. NamespaceState, Microsoft. Azure. Commands. EventHub, Version = 0.6.7.0, Culture = neutral = neutral = NULL]]</span><span class="sxs-lookup"><span data-stu-id="dcc32-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.Commands.EventHub, Version=0.6.7.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="dcc32-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dcc32-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dcc32-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcc32-148">OUTPUTS</span></span>

### <span data-ttu-id="dcc32-149">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="dcc32-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="dcc32-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcc32-150">NOTES</span></span>

## <span data-ttu-id="dcc32-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcc32-151">RELATED LINKS</span></span>
