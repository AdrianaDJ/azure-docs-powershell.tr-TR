---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/enable-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
ms.openlocfilehash: abfa4fa78ecc43921ce779b73575f68654759fe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590930"
---
# <span data-ttu-id="4b266-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4b266-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="4b266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b266-102">SYNOPSIS</span></span>
<span data-ttu-id="4b266-103">Etkinlik günlüğü uyarısını verir ve etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4b266-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b266-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b266-104">SYNTAX</span></span>

### <span data-ttu-id="4b266-105">Enablebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="4b266-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b266-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="4b266-106">EnableByInputObject</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b266-107">Enablebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4b266-107">EnableByResourceId</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b266-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b266-108">DESCRIPTION</span></span>
<span data-ttu-id="4b266-109">**Enable-AzureRmActivityLogAlert** cmdlet 'i etkinlik günlüğü uyarısını etkinleştirmeye ve etiketlerini ayarlamaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4b266-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="4b266-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten düzeltme eki olmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="4b266-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="4b266-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b266-111">EXAMPLES</span></span>

### <span data-ttu-id="4b266-112">Örnek 1: etkinlik günlüğü uyarısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="4b266-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="4b266-113">Bu komut, varsayılan-ActivityLogsAlerts kaynak grubundaki alert1 adındaki etkinlik günlüğü uyarısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="4b266-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="4b266-114">Örnek 2: giriş olarak bir PSActivityLogAlertResource nesnesini kullanarak etkinlik günlüğü uyarısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4b266-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="4b266-115">Bu komut alert1 adındaki bir etkinlik günlüğü uyarısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="4b266-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="4b266-116">Bu, giriş bağımsız değişkeni olarak PSActivityLogAlertResource nesnesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4b266-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="4b266-117">Örnek 3: RESOURCEID parametresini kullanarak ActivityLogAlert 'i etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4b266-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="4b266-118">Bu komut, kanalın RESOURCEID parametresini kullanarak ActivityLogAlert 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="4b266-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="4b266-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b266-119">PARAMETERS</span></span>

### <span data-ttu-id="4b266-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b266-120">-DefaultProfile</span></span>
<span data-ttu-id="4b266-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4b266-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b266-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b266-122">-InputObject</span></span>
<span data-ttu-id="4b266-123">Gerekli adı, kaynak grubu adını ve isteğe bağlı Etiketler özelliklerini ayıklamak için çağrının InputObject Etiketler özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4b266-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="4b266-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b266-124">-Name</span></span>
<span data-ttu-id="4b266-125">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="4b266-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="4b266-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b266-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b266-127">Uyarı kaynağının bulunacağı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4b266-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="4b266-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4b266-128">-ResourceId</span></span>
<span data-ttu-id="4b266-129">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b266-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="4b266-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b266-130">-Confirm</span></span>
<span data-ttu-id="4b266-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b266-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b266-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b266-132">-WhatIf</span></span>
<span data-ttu-id="4b266-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b266-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b266-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b266-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b266-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b266-135">CommonParameters</span></span>
<span data-ttu-id="4b266-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b266-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b266-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b266-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b266-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b266-138">INPUTS</span></span>

### <span data-ttu-id="4b266-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4b266-139">System.String</span></span>

### <span data-ttu-id="4b266-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="4b266-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="4b266-141">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4b266-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4b266-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b266-142">OUTPUTS</span></span>

### <span data-ttu-id="4b266-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="4b266-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="4b266-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b266-144">NOTES</span></span>

## <span data-ttu-id="4b266-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b266-145">RELATED LINKS</span></span>

[<span data-ttu-id="4b266-146">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4b266-146">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4b266-147">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4b266-147">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4b266-148">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4b266-148">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4b266-149">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4b266-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="4b266-150">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="4b266-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="4b266-151">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4b266-151">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)
