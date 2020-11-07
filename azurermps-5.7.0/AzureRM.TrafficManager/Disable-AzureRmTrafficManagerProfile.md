---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 99bff202a67dcc0db6109f3622188e10d250c573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763202"
---
# <span data-ttu-id="8d977-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d977-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="8d977-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d977-102">SYNOPSIS</span></span>
<span data-ttu-id="8d977-103">Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8d977-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d977-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d977-104">SYNTAX</span></span>

### <span data-ttu-id="8d977-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="8d977-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d977-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="8d977-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d977-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d977-107">DESCRIPTION</span></span>
<span data-ttu-id="8d977-108">**Disable-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8d977-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="8d977-109">Düzen nesnesini ardışık düzen veya parametre değeri olarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d977-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="8d977-110">Alternatif olarak, *Name* ve *resourcegroupname* parametrelerini kullanarak profili belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d977-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="8d977-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d977-111">EXAMPLES</span></span>

### <span data-ttu-id="8d977-112">Örnek 1: adla belirtilen bir profili devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="8d977-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="8d977-113">Bu komut, ResourceGroup11 'da ContosoProfile adlı profili devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8d977-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="8d977-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8d977-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="8d977-115">Örnek 2: ardışık düzeni kullanarak profili devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="8d977-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="8d977-116">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profili alır.</span><span class="sxs-lookup"><span data-stu-id="8d977-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="8d977-117">Komut daha sonra bu profili, ardışık düzen işlecini kullanarak **Disable-AzureRmTrafficManagerProfile** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="8d977-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8d977-118">Bu cmdlet profili devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8d977-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="8d977-119">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d977-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8d977-120">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="8d977-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8d977-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d977-121">PARAMETERS</span></span>

### <span data-ttu-id="8d977-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d977-122">-DefaultProfile</span></span>
<span data-ttu-id="8d977-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d977-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d977-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8d977-124">-Force</span></span>
<span data-ttu-id="8d977-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8d977-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d977-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d977-126">-Name</span></span>
<span data-ttu-id="8d977-127">Bu cmdlet 'in devre dışı olduğu Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d977-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="8d977-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d977-128">-ResourceGroupName</span></span>
<span data-ttu-id="8d977-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d977-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8d977-130">Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8d977-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d977-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d977-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="8d977-132">Devre dışı bırakmak için bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d977-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="8d977-133">**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8d977-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="8d977-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="8d977-134">-Confirm</span></span>
<span data-ttu-id="8d977-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8d977-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d977-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d977-136">-WhatIf</span></span>
<span data-ttu-id="8d977-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8d977-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d977-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8d977-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d977-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d977-139">CommonParameters</span></span>
<span data-ttu-id="8d977-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d977-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d977-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d977-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d977-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d977-142">INPUTS</span></span>

### <span data-ttu-id="8d977-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d977-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="8d977-144">Bu cmdlet bir **TrafficManagerProfile** nesnesini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="8d977-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="8d977-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d977-145">OUTPUTS</span></span>

### <span data-ttu-id="8d977-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d977-146">System.Boolean</span></span>

## <span data-ttu-id="8d977-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d977-147">NOTES</span></span>

## <span data-ttu-id="8d977-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d977-148">RELATED LINKS</span></span>

[<span data-ttu-id="8d977-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d977-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8d977-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d977-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8d977-151">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d977-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8d977-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d977-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8d977-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d977-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


