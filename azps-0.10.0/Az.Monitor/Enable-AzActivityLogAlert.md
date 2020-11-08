---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: e2b09005714021bc8b428b93214f30a16a279ce8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935758"
---
# <span data-ttu-id="7e81d-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7e81d-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="7e81d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e81d-102">SYNOPSIS</span></span>
<span data-ttu-id="7e81d-103">Etkinlik günlüğü uyarısını verir ve etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7e81d-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="7e81d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e81d-104">SYNTAX</span></span>

### <span data-ttu-id="7e81d-105">Enablebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="7e81d-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e81d-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="7e81d-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e81d-107">Enablebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="7e81d-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e81d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e81d-108">DESCRIPTION</span></span>
<span data-ttu-id="7e81d-109">**Enable-Azactivilogalert** cmdlet 'i etkinlik günlüğü uyarısını etkinleştirmeye ve etiketlerini ayarlamaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7e81d-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="7e81d-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten düzeltme eki olmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="7e81d-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="7e81d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e81d-111">EXAMPLES</span></span>

### <span data-ttu-id="7e81d-112">Örnek 1: etkinlik günlüğü uyarısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7e81d-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="7e81d-113">Bu komut, varsayılan-ActivityLogsAlerts kaynak grubundaki alert1 adındaki etkinlik günlüğü uyarısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="7e81d-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="7e81d-114">Örnek 2: giriş olarak bir PSActivityLogAlertResource nesnesini kullanarak etkinlik günlüğü uyarısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7e81d-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="7e81d-115">Bu komut alert1 adındaki bir etkinlik günlüğü uyarısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="7e81d-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="7e81d-116">Bu, giriş bağımsız değişkeni olarak PSActivityLogAlertResource nesnesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7e81d-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="7e81d-117">Örnek 3: RESOURCEID parametresini kullanarak ActivityLogAlert 'i etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7e81d-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="7e81d-118">Bu komut, kanalın RESOURCEID parametresini kullanarak ActivityLogAlert 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="7e81d-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="7e81d-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e81d-119">PARAMETERS</span></span>

### <span data-ttu-id="7e81d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e81d-120">-DefaultProfile</span></span>
<span data-ttu-id="7e81d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7e81d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e81d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e81d-122">-InputObject</span></span>
<span data-ttu-id="7e81d-123">Gerekli adı, kaynak grubu adını ve isteğe bağlı Etiketler özelliklerini ayıklamak için çağrının InputObject Etiketler özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7e81d-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="7e81d-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e81d-124">-Name</span></span>
<span data-ttu-id="7e81d-125">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="7e81d-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="7e81d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e81d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7e81d-127">Uyarı kaynağının bulunacağı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7e81d-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="7e81d-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7e81d-128">-ResourceId</span></span>
<span data-ttu-id="7e81d-129">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="7e81d-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="7e81d-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e81d-130">-Confirm</span></span>
<span data-ttu-id="7e81d-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e81d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e81d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e81d-132">-WhatIf</span></span>
<span data-ttu-id="7e81d-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e81d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e81d-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e81d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e81d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e81d-135">CommonParameters</span></span>
<span data-ttu-id="7e81d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e81d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e81d-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7e81d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e81d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e81d-138">INPUTS</span></span>

### <span data-ttu-id="7e81d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7e81d-139">System.String</span></span>

### <span data-ttu-id="7e81d-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="7e81d-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="7e81d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e81d-141">OUTPUTS</span></span>

### <span data-ttu-id="7e81d-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="7e81d-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="7e81d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e81d-143">NOTES</span></span>

## <span data-ttu-id="7e81d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e81d-144">RELATED LINKS</span></span>

[<span data-ttu-id="7e81d-145">Set-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="7e81d-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="7e81d-146">Get-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="7e81d-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="7e81d-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7e81d-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="7e81d-148">Yeni-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="7e81d-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="7e81d-149">Yeni-Azactivilogalertcondition</span><span class="sxs-lookup"><span data-stu-id="7e81d-149">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="7e81d-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7e81d-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)