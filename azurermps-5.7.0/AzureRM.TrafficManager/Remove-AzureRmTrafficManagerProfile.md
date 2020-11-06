---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 459ede802e3a96805bb2c32e4e901592604f03b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589638"
---
# <span data-ttu-id="eb5ca-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ca-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="eb5ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb5ca-102">SYNOPSIS</span></span>
<span data-ttu-id="eb5ca-103">Traffic Manager profilini siler.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb5ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb5ca-104">SYNTAX</span></span>

### <span data-ttu-id="eb5ca-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="eb5ca-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb5ca-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="eb5ca-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb5ca-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb5ca-107">DESCRIPTION</span></span>
<span data-ttu-id="eb5ca-108">**Remove-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profilini siler.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="eb5ca-109">*Name* ve *resourcegroupname* parametrelerini kullanarak silinecek profili belirtin.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="eb5ca-110">Alternatif olarak, *TrafficManagerProfile* parametresini kullanarak bir **TrafficManagerProfile** nesnesi belirtebilirsiniz veya ardışık düzeni kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="eb5ca-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb5ca-111">EXAMPLES</span></span>

### <span data-ttu-id="eb5ca-112">Örnek 1: adla belirtilen bir profili silme</span><span class="sxs-lookup"><span data-stu-id="eb5ca-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="eb5ca-113">Bu komut, ResourceGroup11 'da ContosoProfile adlı profili siler.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="eb5ca-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="eb5ca-115">Örnek 2: ardışık düzeni kullanarak profili silme</span><span class="sxs-lookup"><span data-stu-id="eb5ca-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="eb5ca-116">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profili alır.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="eb5ca-117">Komut daha sonra bu profili, ardışık düzen işlecini kullanarak **Remove-AzureRmTrafficManagerProfile** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eb5ca-118">Bu cmdlet bu profili siler.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="eb5ca-119">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="eb5ca-120">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="eb5ca-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb5ca-121">PARAMETERS</span></span>

### <span data-ttu-id="eb5ca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ca-122">-DefaultProfile</span></span>
<span data-ttu-id="eb5ca-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb5ca-124">-Force</span><span class="sxs-lookup"><span data-stu-id="eb5ca-124">-Force</span></span>
<span data-ttu-id="eb5ca-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb5ca-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="eb5ca-126">-Name</span></span>
<span data-ttu-id="eb5ca-127">Bu cmdlet 'in sildiği Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb5ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb5ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="eb5ca-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="eb5ca-130">Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager profilini siler.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb5ca-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ca-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="eb5ca-132">Silinecek bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="eb5ca-133">**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb5ca-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb5ca-134">-Confirm</span></span>
<span data-ttu-id="eb5ca-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb5ca-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb5ca-136">-WhatIf</span></span>
<span data-ttu-id="eb5ca-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb5ca-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb5ca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb5ca-139">CommonParameters</span></span>
<span data-ttu-id="eb5ca-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb5ca-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb5ca-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb5ca-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb5ca-142">INPUTS</span></span>

### <span data-ttu-id="eb5ca-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ca-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="eb5ca-144">Bu cmdlet bir **TrafficManagerProfile** nesnesini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="eb5ca-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb5ca-145">OUTPUTS</span></span>

### <span data-ttu-id="eb5ca-146">Boole</span><span class="sxs-lookup"><span data-stu-id="eb5ca-146">Boolean</span></span>
<span data-ttu-id="eb5ca-147">Bu cmdlet, başarılı olduysa veya silme işlemi $False başarısız olursa, bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="eb5ca-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="eb5ca-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb5ca-148">NOTES</span></span>

## <span data-ttu-id="eb5ca-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb5ca-149">RELATED LINKS</span></span>

[<span data-ttu-id="eb5ca-150">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ca-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="eb5ca-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ca-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="eb5ca-152">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ca-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="eb5ca-153">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ca-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="eb5ca-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ca-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


