---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: e06482a4bb068ab650a06157f2dad56a9e1ff53c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915695"
---
# <span data-ttu-id="e2a15-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e2a15-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="e2a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2a15-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a15-103">Etkinlik günlüğü uyarısını devre dışı bırakır ve etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e2a15-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="e2a15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2a15-104">SYNTAX</span></span>

### <span data-ttu-id="e2a15-105">Disablebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="e2a15-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a15-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="e2a15-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a15-107">Disablebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e2a15-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2a15-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2a15-108">DESCRIPTION</span></span>
<span data-ttu-id="e2a15-109">**Disable-AzActivityLogAlert** cmdlet 'i devre dışı bırakır ve etkinlik günlüğü uyarılarını ayarlamaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e2a15-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="e2a15-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten düzeltme eki olmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="e2a15-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="e2a15-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2a15-111">EXAMPLES</span></span>

### <span data-ttu-id="e2a15-112">Örnek 1: etkinlik günlüğü uyarısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="e2a15-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="e2a15-113">Bu komut, alert1 adındaki etkinlik günlüğü uyarısını varsayılan-ActivityLogsAlerts kaynak grubunda devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e2a15-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="e2a15-114">Bu komut alert1 adındaki etkinlik günlüğü uyarısı 'nın Etiketler özelliğini değiştirir ve devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e2a15-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="e2a15-115">Örnek 2: giriş olarak bir PSActivityLogAlertResource nesnesini kullanarak etkinlik günlüğü uyarısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="e2a15-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="e2a15-116">Bu komut, alert1 adındaki etkinlik günlüğü uyarısını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e2a15-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="e2a15-117">Bu, giriş bağımsız değişkeni olarak PSActivityLogAlertResource nesnesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e2a15-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="e2a15-118">Örnek 3: RESOURCEID parametresini kullanarak ActivityLogAlert 'i devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="e2a15-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="e2a15-119">Bu komut, kanalın RESOURCEID parametresini kullanarak ActivityLogAlert 'i devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e2a15-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="e2a15-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2a15-120">PARAMETERS</span></span>

### <span data-ttu-id="e2a15-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a15-121">-DefaultProfile</span></span>
<span data-ttu-id="e2a15-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e2a15-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2a15-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2a15-123">-InputObject</span></span>
<span data-ttu-id="e2a15-124">Gerekli adı, kaynak grubu adını ve isteğe bağlı etiket özelliklerini ayıklamak için çağrının InputObject Etiketler özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e2a15-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a15-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2a15-125">-Name</span></span>
<span data-ttu-id="e2a15-126">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="e2a15-126">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a15-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2a15-127">-ResourceGroupName</span></span>
<span data-ttu-id="e2a15-128">Uyarı kaynağının bulunacağı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e2a15-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a15-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e2a15-129">-ResourceId</span></span>
<span data-ttu-id="e2a15-130">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2a15-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a15-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="e2a15-131">-Confirm</span></span>
<span data-ttu-id="e2a15-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e2a15-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2a15-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2a15-133">-WhatIf</span></span>
<span data-ttu-id="e2a15-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2a15-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2a15-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e2a15-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2a15-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a15-136">CommonParameters</span></span>
<span data-ttu-id="e2a15-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2a15-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a15-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2a15-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a15-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2a15-139">INPUTS</span></span>

### <span data-ttu-id="e2a15-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e2a15-140">System.String</span></span>

### <span data-ttu-id="e2a15-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="e2a15-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="e2a15-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2a15-142">OUTPUTS</span></span>

### <span data-ttu-id="e2a15-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="e2a15-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="e2a15-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2a15-144">NOTES</span></span>

## <span data-ttu-id="e2a15-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2a15-145">RELATED LINKS</span></span>

[<span data-ttu-id="e2a15-146">Set-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="e2a15-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="e2a15-147">Get-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="e2a15-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="e2a15-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e2a15-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="e2a15-149">Yeni-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="e2a15-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="e2a15-150">Yeni-Azactivilogalertcondition</span><span class="sxs-lookup"><span data-stu-id="e2a15-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="e2a15-151">Enable-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="e2a15-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
