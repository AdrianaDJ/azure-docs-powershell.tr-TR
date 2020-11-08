---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274000"
---
# <span data-ttu-id="e70b7-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="e70b7-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="e70b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e70b7-102">SYNOPSIS</span></span>
<span data-ttu-id="e70b7-103">IoT toplu uyarısını kapatma</span><span class="sxs-lookup"><span data-stu-id="e70b7-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="e70b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e70b7-104">SYNTAX</span></span>

### <span data-ttu-id="e70b7-105">SolutionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e70b7-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e70b7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e70b7-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e70b7-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="e70b7-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e70b7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e70b7-108">DESCRIPTION</span></span>
<span data-ttu-id="e70b7-109">Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet, IoT Hub aygıtlarında belirli bir belirsiz uyarıyı kapatır.</span><span class="sxs-lookup"><span data-stu-id="e70b7-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="e70b7-110">Derlenmiş uyarıların adı, uyarı türünün ve uyarının belirsiz tarihinin birleşimidir; '/' ile ayrılır.</span><span class="sxs-lookup"><span data-stu-id="e70b7-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="e70b7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e70b7-111">EXAMPLES</span></span>

### <span data-ttu-id="e70b7-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e70b7-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="e70b7-113">"MyResourceGroup" kaynak grubundaki "IoT_SucessfulLocalLogin/2020-03-15" (uyarı türünden bir ad ve Birleşik Tarih)</span><span class="sxs-lookup"><span data-stu-id="e70b7-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="e70b7-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e70b7-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="e70b7-115">Kaynak kimliği "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03" ile toplanmış uyarıyı kapatma</span><span class="sxs-lookup"><span data-stu-id="e70b7-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="e70b7-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e70b7-116">PARAMETERS</span></span>

### <span data-ttu-id="e70b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70b7-117">-DefaultProfile</span></span>
<span data-ttu-id="e70b7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e70b7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e70b7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e70b7-119">-InputObject</span></span>
<span data-ttu-id="e70b7-120">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e70b7-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e70b7-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e70b7-121">-Name</span></span>
<span data-ttu-id="e70b7-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e70b7-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70b7-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e70b7-123">-PassThru</span></span>
<span data-ttu-id="e70b7-124">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="e70b7-124">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e70b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="e70b7-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e70b7-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70b7-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e70b7-127">-ResourceId</span></span>
<span data-ttu-id="e70b7-128">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e70b7-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e70b7-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="e70b7-129">-SolutionName</span></span>
<span data-ttu-id="e70b7-130">Çözüm adı</span><span class="sxs-lookup"><span data-stu-id="e70b7-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70b7-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="e70b7-131">-Confirm</span></span>
<span data-ttu-id="e70b7-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e70b7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e70b7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e70b7-133">-WhatIf</span></span>
<span data-ttu-id="e70b7-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e70b7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e70b7-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e70b7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e70b7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70b7-136">CommonParameters</span></span>
<span data-ttu-id="e70b7-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e70b7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70b7-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e70b7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70b7-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e70b7-139">INPUTS</span></span>

### <span data-ttu-id="e70b7-140">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutionanalytics. Psiotsecurityaggregotalert</span><span class="sxs-lookup"><span data-stu-id="e70b7-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="e70b7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e70b7-141">System.String</span></span>

## <span data-ttu-id="e70b7-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e70b7-142">OUTPUTS</span></span>

### <span data-ttu-id="e70b7-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e70b7-143">System.Boolean</span></span>

## <span data-ttu-id="e70b7-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e70b7-144">NOTES</span></span>

## <span data-ttu-id="e70b7-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e70b7-145">RELATED LINKS</span></span>
