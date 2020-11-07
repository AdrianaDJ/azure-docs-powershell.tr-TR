---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/disable-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: dd84c2b12af850cc38770243df74a6bd25c205f3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939147"
---
# <span data-ttu-id="42f58-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="42f58-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="42f58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42f58-102">SYNOPSIS</span></span>
<span data-ttu-id="42f58-103">Etkinlik günlüğü uyarısını devre dışı bırakır ve etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="42f58-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42f58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42f58-104">SYNTAX</span></span>

### <span data-ttu-id="42f58-105">Disablebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="42f58-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42f58-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="42f58-106">DisableByInputObject</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42f58-107">Disablebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="42f58-107">DisableByResourceId</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42f58-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="42f58-108">DESCRIPTION</span></span>
<span data-ttu-id="42f58-109">**Disable-AzureRmActivityLogAlert** cmdlet 'i devre dışı bırakır ve etkinlik günlüğü uyarılarını ayarlamaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="42f58-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="42f58-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten düzeltme eki olmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="42f58-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="42f58-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42f58-111">EXAMPLES</span></span>

### <span data-ttu-id="42f58-112">Örnek 1: etkinlik günlüğü uyarısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="42f58-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="42f58-113">Bu komut, alert1 adındaki etkinlik günlüğü uyarısını varsayılan-ActivityLogsAlerts kaynak grubunda devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="42f58-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="42f58-114">Bu komut alert1 adındaki etkinlik günlüğü uyarısı 'nın Etiketler özelliğini değiştirir ve devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="42f58-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="42f58-115">Örnek 2: giriş olarak bir PSActivityLogAlertResource nesnesini kullanarak etkinlik günlüğü uyarısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="42f58-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="42f58-116">Bu komut, alert1 adındaki etkinlik günlüğü uyarısını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="42f58-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="42f58-117">Bu, giriş bağımsız değişkeni olarak PSActivityLogAlertResource nesnesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="42f58-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="42f58-118">Örnek 3: RESOURCEID parametresini kullanarak ActivityLogAlert 'i devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="42f58-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="42f58-119">Bu komut, kanalın RESOURCEID parametresini kullanarak ActivityLogAlert 'i devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="42f58-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="42f58-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42f58-120">PARAMETERS</span></span>

### <span data-ttu-id="42f58-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f58-121">-DefaultProfile</span></span>
<span data-ttu-id="42f58-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="42f58-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42f58-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42f58-123">-InputObject</span></span>
<span data-ttu-id="42f58-124">Gerekli adı, kaynak grubu adını ve isteğe bağlı etiket özelliklerini ayıklamak için çağrının InputObject Etiketler özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="42f58-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="42f58-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="42f58-125">-Name</span></span>
<span data-ttu-id="42f58-126">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="42f58-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="42f58-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f58-127">-ResourceGroupName</span></span>
<span data-ttu-id="42f58-128">Uyarı kaynağının bulunacağı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="42f58-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="42f58-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="42f58-129">-ResourceId</span></span>
<span data-ttu-id="42f58-130">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="42f58-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="42f58-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="42f58-131">-Confirm</span></span>
<span data-ttu-id="42f58-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42f58-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42f58-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42f58-133">-WhatIf</span></span>
<span data-ttu-id="42f58-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42f58-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42f58-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42f58-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42f58-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f58-136">CommonParameters</span></span>
<span data-ttu-id="42f58-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42f58-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f58-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f58-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f58-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42f58-139">INPUTS</span></span>

### <span data-ttu-id="42f58-140">System. String</span><span class="sxs-lookup"><span data-stu-id="42f58-140">System.String</span></span>

### <span data-ttu-id="42f58-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="42f58-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="42f58-142">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="42f58-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="42f58-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42f58-143">OUTPUTS</span></span>

### <span data-ttu-id="42f58-144">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="42f58-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="42f58-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42f58-145">NOTES</span></span>

## <span data-ttu-id="42f58-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42f58-146">RELATED LINKS</span></span>

[<span data-ttu-id="42f58-147">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="42f58-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="42f58-148">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="42f58-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="42f58-149">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="42f58-149">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="42f58-150">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="42f58-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="42f58-151">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="42f58-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="42f58-152">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="42f58-152">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
