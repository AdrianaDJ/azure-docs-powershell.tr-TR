---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: adff43beed709db91b2f22bd1072728d3e7a0425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765174"
---
# <span data-ttu-id="1b8ec-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1b8ec-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="1b8ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1b8ec-103">Etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b8ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b8ec-104">SYNTAX</span></span>

### <span data-ttu-id="1b8ec-105">Etkinlik günlüğü uyarısını kaldırma için varsayılan parametreler</span><span class="sxs-lookup"><span data-stu-id="1b8ec-105">Default parameters for remove an activity log alert</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b8ec-106">Bir etkinlik günlüğü uyarılarını kaldırmak için parametre</span><span class="sxs-lookup"><span data-stu-id="1b8ec-106">Parameters to remove an activity log alerts taking value from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b8ec-107">Kanalın değerini kanaldan alan etkinlik günlüğü uyarılarını kaldırmak için parametreler</span><span class="sxs-lookup"><span data-stu-id="1b8ec-107">Parameters to remove an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b8ec-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b8ec-108">DESCRIPTION</span></span>
<span data-ttu-id="1b8ec-109">**Remove-AzureRmActivityLogAlert** cmdlet 'i etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="1b8ec-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten düzeltme eki olmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="1b8ec-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b8ec-111">EXAMPLES</span></span>

### <span data-ttu-id="1b8ec-112">Örnek 1: etkinlik günlüğü uyarısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1b8ec-112">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="1b8ec-113">Ad ve kaynak grubu adını giriş olarak kullanarak etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-113">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="1b8ec-114">Örnek 2: giriş olarak PSActivityLogAlertResource kullanarak etkinlik günlüğü uyarısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1b8ec-114">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="1b8ec-115">PSActivityLogAlertResource öğesini giriş olarak kullanarak etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-115">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="1b8ec-116">Örnek 3: RESOURCEID parametresini kullanarak ActivityLogAlert 'i kaldırma</span><span class="sxs-lookup"><span data-stu-id="1b8ec-116">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="1b8ec-117">Bu komut, kanalın RESOURCEID parametresini kullanarak ActivityLogAlert 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-117">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="1b8ec-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b8ec-118">PARAMETERS</span></span>

### <span data-ttu-id="1b8ec-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b8ec-119">-Name</span></span>
<span data-ttu-id="1b8ec-120">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b8ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="1b8ec-122">Uyarı kaynağının bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-122">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8ec-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b8ec-123">-InputObject</span></span>
<span data-ttu-id="1b8ec-124">Gerekli adı ve kaynak grubu adı özelliklerini ayıklamak için çağrının InputObject etiketleri özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-124">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to remove an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8ec-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1b8ec-125">-ResourceId</span></span>
<span data-ttu-id="1b8ec-126">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-126">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to remove an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8ec-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b8ec-127">-Confirm</span></span>
<span data-ttu-id="1b8ec-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b8ec-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b8ec-129">-DefaultProfile</span></span>
<span data-ttu-id="1b8ec-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b8ec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b8ec-131">-WhatIf</span></span>
<span data-ttu-id="1b8ec-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b8ec-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b8ec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b8ec-134">CommonParameters</span></span>
<span data-ttu-id="1b8ec-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b8ec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b8ec-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b8ec-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b8ec-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b8ec-137">INPUTS</span></span>

## <span data-ttu-id="1b8ec-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b8ec-138">OUTPUTS</span></span>

### <span data-ttu-id="1b8ec-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1b8ec-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="1b8ec-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b8ec-140">NOTES</span></span>

## <span data-ttu-id="1b8ec-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b8ec-141">RELATED LINKS</span></span>

[<span data-ttu-id="1b8ec-142">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1b8ec-142">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="1b8ec-143">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1b8ec-143">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="1b8ec-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1b8ec-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="1b8ec-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1b8ec-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="1b8ec-146">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="1b8ec-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="1b8ec-147">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="1b8ec-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

