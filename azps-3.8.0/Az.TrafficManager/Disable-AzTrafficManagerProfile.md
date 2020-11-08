---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097123"
---
# <span data-ttu-id="6a898-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a898-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="6a898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a898-102">SYNOPSIS</span></span>
<span data-ttu-id="6a898-103">Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="6a898-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="6a898-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a898-104">SYNTAX</span></span>

### <span data-ttu-id="6a898-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="6a898-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a898-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="6a898-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a898-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a898-107">DESCRIPTION</span></span>
<span data-ttu-id="6a898-108">**Disable-AzTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="6a898-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="6a898-109">Düzen nesnesini ardışık düzen veya parametre değeri olarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a898-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="6a898-110">Alternatif olarak, *Name* ve *resourcegroupname* parametrelerini kullanarak profili belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a898-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="6a898-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a898-111">EXAMPLES</span></span>

### <span data-ttu-id="6a898-112">Örnek 1: adla belirtilen bir profili devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="6a898-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="6a898-113">Bu komut, ResourceGroup11 'da ContosoProfile adlı profili devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="6a898-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="6a898-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a898-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="6a898-115">Örnek 2: ardışık düzeni kullanarak profili devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="6a898-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="6a898-116">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profili alır.</span><span class="sxs-lookup"><span data-stu-id="6a898-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="6a898-117">Komut daha sonra bu profili, ardışık düzen işlecini kullanarak **Disable-AzTrafficManagerProfile** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="6a898-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6a898-118">Bu cmdlet profili devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="6a898-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="6a898-119">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a898-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6a898-120">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="6a898-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6a898-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a898-121">PARAMETERS</span></span>

### <span data-ttu-id="6a898-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a898-122">-DefaultProfile</span></span>
<span data-ttu-id="6a898-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a898-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a898-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6a898-124">-Force</span></span>
<span data-ttu-id="6a898-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6a898-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6a898-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a898-126">-Name</span></span>
<span data-ttu-id="6a898-127">Bu cmdlet 'in devre dışı olduğu Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a898-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="6a898-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a898-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a898-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a898-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6a898-130">Bu cmdlet, bu parametrenin belirttiği gruptaki bir Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="6a898-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a898-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a898-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="6a898-132">Devre dışı bırakmak için bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a898-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="6a898-133">**TrafficManagerProfile** nesnesi almak için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a898-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="6a898-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a898-134">-Confirm</span></span>
<span data-ttu-id="6a898-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a898-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a898-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a898-136">-WhatIf</span></span>
<span data-ttu-id="6a898-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a898-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a898-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a898-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a898-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a898-139">CommonParameters</span></span>
<span data-ttu-id="6a898-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a898-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a898-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a898-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a898-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a898-142">INPUTS</span></span>

### <span data-ttu-id="6a898-143">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a898-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="6a898-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a898-144">OUTPUTS</span></span>

### <span data-ttu-id="6a898-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a898-145">System.Boolean</span></span>

## <span data-ttu-id="6a898-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a898-146">NOTES</span></span>

## <span data-ttu-id="6a898-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a898-147">RELATED LINKS</span></span>

[<span data-ttu-id="6a898-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a898-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="6a898-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a898-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="6a898-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a898-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="6a898-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a898-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="6a898-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a898-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


