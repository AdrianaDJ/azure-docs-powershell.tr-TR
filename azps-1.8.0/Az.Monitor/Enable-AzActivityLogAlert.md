---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 4e628affbae7b5356b1cfaacb8970b5315be746d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915691"
---
# <span data-ttu-id="fc5a8-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fc5a8-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="fc5a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5a8-103">Etkinlik günlüğü uyarısını verir ve etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="fc5a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc5a8-104">SYNTAX</span></span>

### <span data-ttu-id="fc5a8-105">Enablebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="fc5a8-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5a8-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc5a8-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5a8-107">Enablebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="fc5a8-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc5a8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc5a8-108">DESCRIPTION</span></span>
<span data-ttu-id="fc5a8-109">**Enable-Azactivilogalert** cmdlet 'i etkinlik günlüğü uyarısını etkinleştirmeye ve etiketlerini ayarlamaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="fc5a8-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten düzeltme eki olmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="fc5a8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc5a8-111">EXAMPLES</span></span>

### <span data-ttu-id="fc5a8-112">Örnek 1: etkinlik günlüğü uyarısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="fc5a8-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="fc5a8-113">Bu komut, varsayılan-ActivityLogsAlerts kaynak grubundaki alert1 adındaki etkinlik günlüğü uyarısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="fc5a8-114">Örnek 2: giriş olarak bir PSActivityLogAlertResource nesnesini kullanarak etkinlik günlüğü uyarısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="fc5a8-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="fc5a8-115">Bu komut alert1 adındaki bir etkinlik günlüğü uyarısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="fc5a8-116">Bu, giriş bağımsız değişkeni olarak PSActivityLogAlertResource nesnesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="fc5a8-117">Örnek 3: RESOURCEID parametresini kullanarak ActivityLogAlert 'i etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="fc5a8-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="fc5a8-118">Bu komut, kanalın RESOURCEID parametresini kullanarak ActivityLogAlert 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="fc5a8-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc5a8-119">PARAMETERS</span></span>

### <span data-ttu-id="fc5a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5a8-120">-DefaultProfile</span></span>
<span data-ttu-id="fc5a8-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fc5a8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc5a8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc5a8-122">-InputObject</span></span>
<span data-ttu-id="fc5a8-123">Gerekli adı, kaynak grubu adını ve isteğe bağlı Etiketler özelliklerini ayıklamak için çağrının InputObject Etiketler özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="fc5a8-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc5a8-124">-Name</span></span>
<span data-ttu-id="fc5a8-125">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="fc5a8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc5a8-126">-ResourceGroupName</span></span>
<span data-ttu-id="fc5a8-127">Uyarı kaynağının bulunacağı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="fc5a8-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fc5a8-128">-ResourceId</span></span>
<span data-ttu-id="fc5a8-129">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="fc5a8-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc5a8-130">-Confirm</span></span>
<span data-ttu-id="fc5a8-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc5a8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5a8-132">-WhatIf</span></span>
<span data-ttu-id="fc5a8-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc5a8-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc5a8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5a8-135">CommonParameters</span></span>
<span data-ttu-id="fc5a8-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc5a8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5a8-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc5a8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5a8-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc5a8-138">INPUTS</span></span>

### <span data-ttu-id="fc5a8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fc5a8-139">System.String</span></span>

### <span data-ttu-id="fc5a8-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="fc5a8-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="fc5a8-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc5a8-141">OUTPUTS</span></span>

### <span data-ttu-id="fc5a8-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="fc5a8-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="fc5a8-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc5a8-143">NOTES</span></span>

## <span data-ttu-id="fc5a8-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc5a8-144">RELATED LINKS</span></span>

[<span data-ttu-id="fc5a8-145">Set-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="fc5a8-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="fc5a8-146">Get-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="fc5a8-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="fc5a8-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fc5a8-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="fc5a8-148">Yeni-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="fc5a8-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="fc5a8-149">Yeni-Azactivilogalertcondition</span><span class="sxs-lookup"><span data-stu-id="fc5a8-149">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="fc5a8-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fc5a8-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
