---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 19f226d79e0de1b32aacae2beda22eae20d40afa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753862"
---
# <span data-ttu-id="1a690-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1a690-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="1a690-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a690-102">SYNOPSIS</span></span>
<span data-ttu-id="1a690-103">Traffic Manager profilini siler.</span><span class="sxs-lookup"><span data-stu-id="1a690-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="1a690-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a690-104">SYNTAX</span></span>

### <span data-ttu-id="1a690-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="1a690-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a690-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="1a690-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a690-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a690-107">DESCRIPTION</span></span>
<span data-ttu-id="1a690-108">**Remove-AzTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profilini siler.</span><span class="sxs-lookup"><span data-stu-id="1a690-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="1a690-109">*Name* ve *resourcegroupname* parametrelerini kullanarak silinecek profili belirtin.</span><span class="sxs-lookup"><span data-stu-id="1a690-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1a690-110">Alternatif olarak, *TrafficManagerProfile* parametresini kullanarak bir **TrafficManagerProfile** nesnesi belirtebilirsiniz veya ardışık düzeni kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a690-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="1a690-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a690-111">EXAMPLES</span></span>

### <span data-ttu-id="1a690-112">Örnek 1: adla belirtilen bir profili silme</span><span class="sxs-lookup"><span data-stu-id="1a690-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="1a690-113">Bu komut, ResourceGroup11 'da ContosoProfile adlı profili siler.</span><span class="sxs-lookup"><span data-stu-id="1a690-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="1a690-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a690-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="1a690-115">Örnek 2: ardışık düzeni kullanarak profili silme</span><span class="sxs-lookup"><span data-stu-id="1a690-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="1a690-116">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profili alır.</span><span class="sxs-lookup"><span data-stu-id="1a690-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="1a690-117">Komut daha sonra bu profili, ardışık düzen işlecini kullanarak **Remove-AzTrafficManagerProfile** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="1a690-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1a690-118">Bu cmdlet bu profili siler.</span><span class="sxs-lookup"><span data-stu-id="1a690-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="1a690-119">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a690-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1a690-120">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="1a690-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1a690-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a690-121">PARAMETERS</span></span>

### <span data-ttu-id="1a690-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a690-122">-DefaultProfile</span></span>
<span data-ttu-id="1a690-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a690-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a690-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1a690-124">-Force</span></span>
<span data-ttu-id="1a690-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="1a690-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a690-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a690-126">-Name</span></span>
<span data-ttu-id="1a690-127">Bu cmdlet 'in sildiği Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a690-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a690-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a690-128">-ResourceGroupName</span></span>
<span data-ttu-id="1a690-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a690-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1a690-130">Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager profilini siler.</span><span class="sxs-lookup"><span data-stu-id="1a690-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a690-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1a690-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="1a690-132">Silinecek bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a690-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="1a690-133">**TrafficManagerProfile** nesnesi almak için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a690-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a690-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a690-134">-Confirm</span></span>
<span data-ttu-id="1a690-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a690-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a690-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a690-136">-WhatIf</span></span>
<span data-ttu-id="1a690-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a690-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a690-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a690-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a690-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a690-139">CommonParameters</span></span>
<span data-ttu-id="1a690-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a690-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a690-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a690-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a690-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a690-142">INPUTS</span></span>

### <span data-ttu-id="1a690-143">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1a690-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="1a690-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a690-144">OUTPUTS</span></span>

### <span data-ttu-id="1a690-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a690-145">System.Boolean</span></span>

## <span data-ttu-id="1a690-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a690-146">NOTES</span></span>

## <span data-ttu-id="1a690-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a690-147">RELATED LINKS</span></span>

[<span data-ttu-id="1a690-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1a690-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="1a690-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1a690-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="1a690-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1a690-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="1a690-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1a690-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="1a690-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1a690-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


