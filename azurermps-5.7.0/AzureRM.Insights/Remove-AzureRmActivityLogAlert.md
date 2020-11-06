---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: b712363b2b4e1d610f00f1111c48145debe084a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592493"
---
# <span data-ttu-id="39ffb-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="39ffb-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="39ffb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="39ffb-103">Etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="39ffb-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39ffb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39ffb-104">SYNTAX</span></span>

### <span data-ttu-id="39ffb-105">Removebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="39ffb-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39ffb-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="39ffb-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39ffb-107">Removebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="39ffb-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39ffb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="39ffb-108">DESCRIPTION</span></span>
<span data-ttu-id="39ffb-109">**Remove-AzureRmActivityLogAlert** cmdlet 'i etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="39ffb-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="39ffb-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağın gerçekten düzeltme eki olmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="39ffb-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

<span data-ttu-id="39ffb-111">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="39ffb-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="39ffb-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39ffb-112">EXAMPLES</span></span>

### <span data-ttu-id="39ffb-113">Örnek 1: etkinlik günlüğü uyarısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="39ffb-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="39ffb-114">Ad ve kaynak grubu adını giriş olarak kullanarak etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="39ffb-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="39ffb-115">Örnek 2: giriş olarak PSActivityLogAlertResource kullanarak etkinlik günlüğü uyarısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="39ffb-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="39ffb-116">PSActivityLogAlertResource öğesini giriş olarak kullanarak etkinlik günlüğü uyarısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="39ffb-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="39ffb-117">Örnek 3: RESOURCEID parametresini kullanarak ActivityLogAlert 'i kaldırma</span><span class="sxs-lookup"><span data-stu-id="39ffb-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="39ffb-118">Bu komut, kanalın RESOURCEID parametresini kullanarak ActivityLogAlert 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="39ffb-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="39ffb-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39ffb-119">PARAMETERS</span></span>

### <span data-ttu-id="39ffb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ffb-120">-DefaultProfile</span></span>
<span data-ttu-id="39ffb-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="39ffb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ffb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39ffb-122">-InputObject</span></span>
<span data-ttu-id="39ffb-123">Gerekli adı ve kaynak grubu adı özelliklerini ayıklamak için çağrının InputObject etiketleri özelliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="39ffb-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39ffb-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="39ffb-124">-Name</span></span>
<span data-ttu-id="39ffb-125">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="39ffb-125">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39ffb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ffb-126">-ResourceGroupName</span></span>
<span data-ttu-id="39ffb-127">Uyarı kaynağının bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="39ffb-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39ffb-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="39ffb-128">-ResourceId</span></span>
<span data-ttu-id="39ffb-129">Aramanın RESOURCEID etiketleri özelliğini ayarlayarak, gerekli adı, kaynak grubu adı özelliklerini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="39ffb-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39ffb-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="39ffb-130">-Confirm</span></span>
<span data-ttu-id="39ffb-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="39ffb-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ffb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ffb-132">-WhatIf</span></span>
<span data-ttu-id="39ffb-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="39ffb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39ffb-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="39ffb-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ffb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ffb-135">CommonParameters</span></span>
<span data-ttu-id="39ffb-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39ffb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ffb-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ffb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ffb-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39ffb-138">INPUTS</span></span>

### <span data-ttu-id="39ffb-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="39ffb-139">None</span></span>
<span data-ttu-id="39ffb-140">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="39ffb-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="39ffb-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39ffb-141">OUTPUTS</span></span>

### <span data-ttu-id="39ffb-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="39ffb-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="39ffb-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39ffb-143">NOTES</span></span>

## <span data-ttu-id="39ffb-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39ffb-144">RELATED LINKS</span></span>

[<span data-ttu-id="39ffb-145">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="39ffb-145">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="39ffb-146">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="39ffb-146">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="39ffb-147">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="39ffb-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="39ffb-148">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="39ffb-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="39ffb-149">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="39ffb-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="39ffb-150">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="39ffb-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

