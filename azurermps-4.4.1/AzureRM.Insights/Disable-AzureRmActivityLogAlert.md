---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: cf920fe8fbe235a2c003bebc0cdecf1a480926ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764829"
---
# <span data-ttu-id="a7392-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a7392-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="a7392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7392-102">SYNOPSIS</span></span>
<span data-ttu-id="a7392-103">Etkinlik günlüğü uyarısını devre dışı bırakır ve etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a7392-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7392-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7392-104">SYNTAX</span></span>

### <span data-ttu-id="a7392-105">Etkinlik günlüğü uyarısını devre dışı bırakma için varsayılan parametreler</span><span class="sxs-lookup"><span data-stu-id="a7392-105">Default parameters for disable an activity log alert</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7392-106">Bir etkinlik günlüğü uyarılarını kanaldan devre dışı bırakma parametreleri</span><span class="sxs-lookup"><span data-stu-id="a7392-106">Parameters to disable an activity log alerts taking value from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7392-107">Kanalın değerini kanaldan alan etkinlik günlüğü uyarılarını devre dışı bırakma parametreleri</span><span class="sxs-lookup"><span data-stu-id="a7392-107">Parameters to disable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7392-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7392-108">DESCRIPTION</span></span>
<span data-ttu-id="a7392-109">**Disable-AzureRmActivityLogAlert** cmdlet 'i devre dışı bırakır ve etkinlik günlüğü uyarılarını ayarlamaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a7392-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="a7392-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten düzeltme eki olmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="a7392-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="a7392-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7392-111">EXAMPLES</span></span>

### <span data-ttu-id="a7392-112">Örnek 1: etkinlik günlüğü uyarısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a7392-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="a7392-113">Bu komut, alert1 adındaki etkinlik günlüğü uyarısını varsayılan-ActivityLogsAlerts kaynak grubunda devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a7392-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

<span data-ttu-id="a7392-114">Bu komut alert1 adındaki etkinlik günlüğü uyarısı 'nın Etiketler özelliğini değiştirir ve devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a7392-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="a7392-115">Örnek 2: giriş olarak bir PSActivityLogAlertResource nesnesini kullanarak etkinlik günlüğü uyarısını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a7392-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="a7392-116">Bu komut, alert1 adındaki etkinlik günlüğü uyarısını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a7392-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="a7392-117">Bu, giriş bağımsız değişkeni olarak PSActivityLogAlertResource nesnesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a7392-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="a7392-118">Örnek 3: RESOURCEID parametresini kullanarak ActivityLogAlert 'i devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a7392-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="a7392-119">Bu komut, kanalın RESOURCEID parametresini kullanarak ActivityLogAlert 'i devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a7392-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="a7392-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7392-120">PARAMETERS</span></span>

### <span data-ttu-id="a7392-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7392-121">-Name</span></span>
<span data-ttu-id="a7392-122">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="a7392-122">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7392-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7392-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7392-124">Uyarı kaynağının bulunacağı kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a7392-124">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7392-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7392-125">-InputObject</span></span>
<span data-ttu-id="a7392-126">Gerekli adı, kaynak grubu adını ve isteğe bağlı etiket özelliklerini ayıklamak için çağrının InputObject Etiketler özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a7392-126">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to disable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7392-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a7392-127">-ResourceId</span></span>
<span data-ttu-id="a7392-128">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="a7392-128">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to disable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7392-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7392-129">-Confirm</span></span>
<span data-ttu-id="a7392-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7392-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7392-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7392-131">-DefaultProfile</span></span>
<span data-ttu-id="a7392-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7392-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7392-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7392-133">-WhatIf</span></span>
<span data-ttu-id="a7392-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7392-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7392-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7392-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7392-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7392-136">CommonParameters</span></span>
<span data-ttu-id="a7392-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7392-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7392-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7392-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7392-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7392-139">INPUTS</span></span>

## <span data-ttu-id="a7392-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7392-140">OUTPUTS</span></span>

### <span data-ttu-id="a7392-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a7392-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a7392-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7392-142">NOTES</span></span>

## <span data-ttu-id="a7392-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7392-143">RELATED LINKS</span></span>

[<span data-ttu-id="a7392-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a7392-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a7392-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a7392-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a7392-146">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a7392-146">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a7392-147">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a7392-147">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="a7392-148">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a7392-148">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="a7392-149">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a7392-149">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
