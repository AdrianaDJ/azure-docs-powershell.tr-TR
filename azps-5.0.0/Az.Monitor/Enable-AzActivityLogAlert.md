---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 6e3414efd21b1dd333f91e24333cda05ea650600
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280046"
---
# <span data-ttu-id="deea7-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="deea7-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="deea7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deea7-102">SYNOPSIS</span></span>
<span data-ttu-id="deea7-103">Etkinlik günlüğü uyarısını verir ve etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="deea7-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="deea7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="deea7-104">SYNTAX</span></span>

### <span data-ttu-id="deea7-105">Enablebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="deea7-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deea7-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="deea7-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deea7-107">Enablebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="deea7-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="deea7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="deea7-108">DESCRIPTION</span></span>
<span data-ttu-id="deea7-109">**Enable-Azactivilogalert** cmdlet 'i etkinlik günlüğü uyarısını etkinleştirmeye ve etiketlerini ayarlamaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="deea7-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="deea7-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten düzeltme eki olmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="deea7-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="deea7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="deea7-111">EXAMPLES</span></span>

### <span data-ttu-id="deea7-112">Örnek 1: etkinlik günlüğü uyarısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="deea7-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="deea7-113">Bu komut, varsayılan-ActivityLogsAlerts kaynak grubundaki alert1 adındaki etkinlik günlüğü uyarısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="deea7-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="deea7-114">Örnek 2: giriş olarak bir PSActivityLogAlertResource nesnesini kullanarak etkinlik günlüğü uyarısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="deea7-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="deea7-115">Bu komut alert1 adındaki bir etkinlik günlüğü uyarısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="deea7-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="deea7-116">Bu, giriş bağımsız değişkeni olarak PSActivityLogAlertResource nesnesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="deea7-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="deea7-117">Örnek 3: RESOURCEID parametresini kullanarak ActivityLogAlert 'i etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="deea7-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="deea7-118">Bu komut, kanalın RESOURCEID parametresini kullanarak ActivityLogAlert 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="deea7-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="deea7-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="deea7-119">PARAMETERS</span></span>

### <span data-ttu-id="deea7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deea7-120">-DefaultProfile</span></span>
<span data-ttu-id="deea7-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="deea7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="deea7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="deea7-122">-InputObject</span></span>
<span data-ttu-id="deea7-123">Gerekli adı, kaynak grubu adını ve isteğe bağlı Etiketler özelliklerini ayıklamak için çağrının InputObject Etiketler özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="deea7-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="deea7-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="deea7-124">-Name</span></span>
<span data-ttu-id="deea7-125">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="deea7-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deea7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deea7-126">-ResourceGroupName</span></span>
<span data-ttu-id="deea7-127">Uyarı kaynağının bulunacağı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="deea7-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deea7-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="deea7-128">-ResourceId</span></span>
<span data-ttu-id="deea7-129">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="deea7-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deea7-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="deea7-130">-Confirm</span></span>
<span data-ttu-id="deea7-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="deea7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deea7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deea7-132">-WhatIf</span></span>
<span data-ttu-id="deea7-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="deea7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="deea7-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="deea7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deea7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deea7-135">CommonParameters</span></span>
<span data-ttu-id="deea7-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="deea7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deea7-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="deea7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deea7-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="deea7-138">INPUTS</span></span>

### <span data-ttu-id="deea7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="deea7-139">System.String</span></span>

### <span data-ttu-id="deea7-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="deea7-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="deea7-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="deea7-141">OUTPUTS</span></span>

### <span data-ttu-id="deea7-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="deea7-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="deea7-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="deea7-143">NOTES</span></span>

## <span data-ttu-id="deea7-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="deea7-144">RELATED LINKS</span></span>

[<span data-ttu-id="deea7-145">Set-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="deea7-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="deea7-146">Get-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="deea7-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="deea7-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="deea7-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="deea7-148">Yeni-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="deea7-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="deea7-149">Yeni-Azactivilogalertcondition</span><span class="sxs-lookup"><span data-stu-id="deea7-149">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="deea7-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="deea7-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
