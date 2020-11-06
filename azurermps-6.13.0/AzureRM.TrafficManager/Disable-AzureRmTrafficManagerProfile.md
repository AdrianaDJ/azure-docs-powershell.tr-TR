---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: e714caedb86bd647ccc0692c47233833bc2db867
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587117"
---
# <span data-ttu-id="7f92f-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f92f-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="7f92f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f92f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f92f-103">Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="7f92f-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f92f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f92f-104">SYNTAX</span></span>

### <span data-ttu-id="7f92f-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="7f92f-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f92f-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="7f92f-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f92f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f92f-107">DESCRIPTION</span></span>
<span data-ttu-id="7f92f-108">**Disable-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="7f92f-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7f92f-109">Düzen nesnesini ardışık düzen veya parametre değeri olarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f92f-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="7f92f-110">Alternatif olarak, *Name* ve *resourcegroupname* parametrelerini kullanarak profili belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f92f-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="7f92f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f92f-111">EXAMPLES</span></span>

### <span data-ttu-id="7f92f-112">Örnek 1: adla belirtilen bir profili devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7f92f-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7f92f-113">Bu komut, ResourceGroup11 'da ContosoProfile adlı profili devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="7f92f-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7f92f-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f92f-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="7f92f-115">Örnek 2: ardışık düzeni kullanarak profili devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7f92f-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="7f92f-116">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profili alır.</span><span class="sxs-lookup"><span data-stu-id="7f92f-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7f92f-117">Komut daha sonra bu profili, ardışık düzen işlecini kullanarak **Disable-AzureRmTrafficManagerProfile** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="7f92f-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7f92f-118">Bu cmdlet profili devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="7f92f-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="7f92f-119">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f92f-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7f92f-120">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="7f92f-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7f92f-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f92f-121">PARAMETERS</span></span>

### <span data-ttu-id="7f92f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f92f-122">-DefaultProfile</span></span>
<span data-ttu-id="7f92f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f92f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f92f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7f92f-124">-Force</span></span>
<span data-ttu-id="7f92f-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7f92f-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f92f-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f92f-126">-Name</span></span>
<span data-ttu-id="7f92f-127">Bu cmdlet 'in devre dışı olduğu Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f92f-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="7f92f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f92f-128">-ResourceGroupName</span></span>
<span data-ttu-id="7f92f-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f92f-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7f92f-130">Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="7f92f-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f92f-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f92f-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="7f92f-132">Devre dışı bırakmak için bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f92f-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="7f92f-133">**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7f92f-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="7f92f-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f92f-134">-Confirm</span></span>
<span data-ttu-id="7f92f-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f92f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f92f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f92f-136">-WhatIf</span></span>
<span data-ttu-id="7f92f-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f92f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f92f-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f92f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f92f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f92f-139">CommonParameters</span></span>
<span data-ttu-id="7f92f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f92f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f92f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f92f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f92f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f92f-142">INPUTS</span></span>

### <span data-ttu-id="7f92f-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f92f-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="7f92f-144">Bu cmdlet bir **TrafficManagerProfile** nesnesini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="7f92f-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="7f92f-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f92f-145">OUTPUTS</span></span>

### <span data-ttu-id="7f92f-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f92f-146">System.Boolean</span></span>

## <span data-ttu-id="7f92f-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f92f-147">NOTES</span></span>

## <span data-ttu-id="7f92f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f92f-148">RELATED LINKS</span></span>

[<span data-ttu-id="7f92f-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f92f-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7f92f-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f92f-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7f92f-151">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f92f-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7f92f-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f92f-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7f92f-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f92f-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


