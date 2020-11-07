---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: c75b456021368ea72a72bd0b0fea07a0f13d06dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760809"
---
# <span data-ttu-id="e4875-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e4875-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="e4875-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4875-102">SYNOPSIS</span></span>
<span data-ttu-id="e4875-103">Belirtilen olay hub ad boşluğunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e4875-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="e4875-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4875-104">SYNTAX</span></span>

### <span data-ttu-id="e4875-105">NamespaceParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e4875-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4875-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4875-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4875-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4875-107">DESCRIPTION</span></span>
<span data-ttu-id="e4875-108">Set-AzEventHubNamespace cmdlet 'i belirtilen olay hub 'Larının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e4875-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="e4875-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4875-109">EXAMPLES</span></span>

### <span data-ttu-id="e4875-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e4875-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="e4875-111">\`Mynamespacename ad alanının durumunu \` oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e4875-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="e4875-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e4875-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="e4875-113">\` \` Autoinir = Enabled ve MaximumThroughputUnits = 10 olan mynamespacename 'in durumunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="e4875-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="e4875-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4875-114">PARAMETERS</span></span>

### <span data-ttu-id="e4875-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4875-115">-DefaultProfile</span></span>
<span data-ttu-id="e4875-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4875-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4875-117">-Enableautoinir</span><span class="sxs-lookup"><span data-stu-id="e4875-117">-EnableAutoInflate</span></span>
<span data-ttu-id="e4875-118">Autoinir özelliğinin etkinleştirilip etkinleştirilmediğini gösterir</span><span class="sxs-lookup"><span data-stu-id="e4875-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="e4875-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="e4875-119">-Location</span></span>
<span data-ttu-id="e4875-120">EventHub ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="e4875-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="e4875-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="e4875-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="e4875-122">Üretilen iş birimlerinin üst limiti otomatik değer değeri etkinleştirildiğinde, değer 0-20 üretilen iş birimi cinsinden olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e4875-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="e4875-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4875-123">-Name</span></span>
<span data-ttu-id="e4875-124">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="e4875-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="e4875-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4875-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4875-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e4875-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4875-127">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="e4875-127">-SkuCapacity</span></span>
<span data-ttu-id="e4875-128">Eventhub üretim birimleri.</span><span class="sxs-lookup"><span data-stu-id="e4875-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="e4875-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e4875-129">-SkuName</span></span>
<span data-ttu-id="e4875-130">Ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="e4875-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="e4875-131">Durumlu</span><span class="sxs-lookup"><span data-stu-id="e4875-131">-State</span></span>
<span data-ttu-id="e4875-132">Ad alanını devre dışı bırakma/etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="e4875-132">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="e4875-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e4875-133">-Tag</span></span>
<span data-ttu-id="e4875-134">Kaynak etiketini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="e4875-134">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="e4875-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4875-135">-Confirm</span></span>
<span data-ttu-id="e4875-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4875-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4875-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4875-137">-WhatIf</span></span>
<span data-ttu-id="e4875-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4875-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4875-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4875-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4875-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4875-140">CommonParameters</span></span>
<span data-ttu-id="e4875-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4875-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4875-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4875-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4875-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4875-143">INPUTS</span></span>

### <span data-ttu-id="e4875-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e4875-144">System.String</span></span>

### <span data-ttu-id="e4875-145">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4875-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e4875-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. modeller. NamespaceState, Microsoft. Azure. PowerShell. cmdlet. EventHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e4875-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e4875-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4875-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e4875-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4875-148">OUTPUTS</span></span>

### <span data-ttu-id="e4875-149">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e4875-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e4875-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4875-150">NOTES</span></span>

## <span data-ttu-id="e4875-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4875-151">RELATED LINKS</span></span>
