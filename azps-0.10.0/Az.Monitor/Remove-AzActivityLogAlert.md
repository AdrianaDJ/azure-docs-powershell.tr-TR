---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 0bcf5c5ccc871867f89687558777c9550a0b9185
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935689"
---
# <span data-ttu-id="52d6f-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="52d6f-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="52d6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="52d6f-103">Etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52d6f-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="52d6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52d6f-104">SYNTAX</span></span>

### <span data-ttu-id="52d6f-105">Removebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="52d6f-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52d6f-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="52d6f-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52d6f-107">Removebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="52d6f-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52d6f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="52d6f-108">DESCRIPTION</span></span>
<span data-ttu-id="52d6f-109">**Remove-AzActivityLogAlert** cmdlet 'i etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52d6f-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="52d6f-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten düzeltme eki olmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="52d6f-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="52d6f-111">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="52d6f-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="52d6f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52d6f-112">EXAMPLES</span></span>

### <span data-ttu-id="52d6f-113">Örnek 1: etkinlik günlüğü uyarısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="52d6f-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="52d6f-114">Ad ve kaynak grubu adını giriş olarak kullanarak etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52d6f-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="52d6f-115">Örnek 2: giriş olarak PSActivityLogAlertResource kullanarak etkinlik günlüğü uyarısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="52d6f-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="52d6f-116">PSActivityLogAlertResource öğesini giriş olarak kullanarak etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52d6f-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="52d6f-117">Örnek 3: RESOURCEID parametresini kullanarak ActivityLogAlert 'i kaldırma</span><span class="sxs-lookup"><span data-stu-id="52d6f-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="52d6f-118">Bu komut, kanalın RESOURCEID parametresini kullanarak ActivityLogAlert 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52d6f-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="52d6f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52d6f-119">PARAMETERS</span></span>

### <span data-ttu-id="52d6f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d6f-120">-DefaultProfile</span></span>
<span data-ttu-id="52d6f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="52d6f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52d6f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52d6f-122">-InputObject</span></span>
<span data-ttu-id="52d6f-123">Gerekli adı ve kaynak grubu adı özelliklerini ayıklamak için çağrının InputObject etiketleri özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="52d6f-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52d6f-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="52d6f-124">-Name</span></span>
<span data-ttu-id="52d6f-125">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="52d6f-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d6f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d6f-126">-ResourceGroupName</span></span>
<span data-ttu-id="52d6f-127">Uyarı kaynağının bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="52d6f-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d6f-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="52d6f-128">-ResourceId</span></span>
<span data-ttu-id="52d6f-129">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="52d6f-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d6f-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="52d6f-130">-Confirm</span></span>
<span data-ttu-id="52d6f-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52d6f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52d6f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52d6f-132">-WhatIf</span></span>
<span data-ttu-id="52d6f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52d6f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52d6f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52d6f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52d6f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d6f-135">CommonParameters</span></span>
<span data-ttu-id="52d6f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52d6f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d6f-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="52d6f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d6f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52d6f-138">INPUTS</span></span>

### <span data-ttu-id="52d6f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="52d6f-139">System.String</span></span>

### <span data-ttu-id="52d6f-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="52d6f-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="52d6f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52d6f-141">OUTPUTS</span></span>

### <span data-ttu-id="52d6f-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="52d6f-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="52d6f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52d6f-143">NOTES</span></span>

## <span data-ttu-id="52d6f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52d6f-144">RELATED LINKS</span></span>

[<span data-ttu-id="52d6f-145">Enable-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="52d6f-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="52d6f-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="52d6f-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="52d6f-147">Set-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="52d6f-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="52d6f-148">Get-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="52d6f-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="52d6f-149">Yeni-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="52d6f-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="52d6f-150">Yeni-Azactivilogalertcondition</span><span class="sxs-lookup"><span data-stu-id="52d6f-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

