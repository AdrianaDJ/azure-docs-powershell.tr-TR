---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107411"
---
# <span data-ttu-id="7ebf0-101">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7ebf0-101">Remove-WAPackVMRole</span></span>

## <span data-ttu-id="7ebf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ebf0-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebf0-103">Sanal makine rolü nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-103">Removes virtual machine role objects.</span></span>

## <span data-ttu-id="7ebf0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ebf0-104">SYNTAX</span></span>

### <span data-ttu-id="7ebf0-105">FromVMRoleObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7ebf0-105">FromVMRoleObject (Default)</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ebf0-106">Fromchoparlör hizmeti</span><span class="sxs-lookup"><span data-stu-id="7ebf0-106">FromCloudService</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ebf0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ebf0-107">DESCRIPTION</span></span>
<span data-ttu-id="7ebf0-108">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7ebf0-109">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7ebf0-110">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7ebf0-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7ebf0-111">**Remove-WAPackVMRole** cmdlet 'i sanal makine rol nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-111">The **Remove-WAPackVMRole** cmdlet removes virtual machine role objects.</span></span>

## <span data-ttu-id="7ebf0-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ebf0-112">EXAMPLES</span></span>

### <span data-ttu-id="7ebf0-113">Örnek 1: sanal makine rolünü kaldırma (WAP Portalı kullanılarak oluşturulmuş)</span><span class="sxs-lookup"><span data-stu-id="7ebf0-113">Example 1: Remove a virtual machine role (which was created using the WAP portal)</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

<span data-ttu-id="7ebf0-114">İlk komut ContosoVMRole01 adındaki sanal makine rolünü **Get-WAPackVMRole** cmdlet 'ini kullanarak alır ve bu nesneyi $VMRole değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-114">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="7ebf0-115">İkinci komut, $VMRole depolanan sanal makine rolünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-115">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="7ebf0-116">Komut sizden onaylamanızı ister. Bu sanal makine rolünün WAP Portalı kullanılarak oluşturulduğunu varsayarsak, bulut hizmeti adını belirtmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-116">The command prompts you for confirmation.Assuming this virtual machine role was created using the WAP portal, there's no need to specify the cloud service name.</span></span>

### <span data-ttu-id="7ebf0-117">Örnek 2: el ile bulut hizmeti oluşturulduktan sonra oluşturulan bir sanal makine rolünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="7ebf0-117">Example 2: Remove a virtual machine role which was created after manually creating a cloud service</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

<span data-ttu-id="7ebf0-118">İlk komut, **Get-WAPackVMRole** cmdlet 'ini kullanarak "ContosoVMRole02" adlı sanal makine rolünü alır ve bu nesneyi $VMRole değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-118">The first command gets the virtual machine role named "ContosoVMRole02" by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="7ebf0-119">İkinci komut, $VMRole depolanan sanal makine rolünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-119">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="7ebf0-120">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="7ebf0-121">Bu sanal makine rolünün Portal kullanılarak oluşturulmamış olduğunu varsayarsak, kullanıcının bulut hizmeti adını belirtmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-121">Assuming this virtual machine role was not created using the portal, the user needs to specify the cloud service name.</span></span>
<span data-ttu-id="7ebf0-122">Bu durumda, "ContosoCloudService02".</span><span class="sxs-lookup"><span data-stu-id="7ebf0-122">In this case named "ContosoCloudService02".</span></span>

### <span data-ttu-id="7ebf0-123">Örnek 3: onaysız sanal makine rolünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="7ebf0-123">Example 3: Remove a virtual machine role without confirmation</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

<span data-ttu-id="7ebf0-124">İlk komut ContosoVMRole03 adındaki bulut hizmetini **Get-WAPackVMRole** cmdlet 'ini kullanarak alır ve bu nesneyi $VMRole değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-124">The first command gets the cloud service named ContosoVMRole03 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="7ebf0-125">İkinci komut, $VMRole depolanan sanal makine rolünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-125">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="7ebf0-126">Bu komut *Force* parametresini içerir.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-126">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="7ebf0-127">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-127">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7ebf0-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ebf0-128">PARAMETERS</span></span>

### <span data-ttu-id="7ebf0-129">-Cloudhizmetadı</span><span class="sxs-lookup"><span data-stu-id="7ebf0-129">-CloudServiceName</span></span>
<span data-ttu-id="7ebf0-130">Sanal makine rolünün bulut hizmeti adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-130">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebf0-131">-Force</span><span class="sxs-lookup"><span data-stu-id="7ebf0-131">-Force</span></span>
<span data-ttu-id="7ebf0-132">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ebf0-133">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7ebf0-133">-PassThru</span></span>
<span data-ttu-id="7ebf0-134">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7ebf0-135">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7ebf0-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="7ebf0-136">-Profile</span></span>
<span data-ttu-id="7ebf0-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7ebf0-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebf0-139">-VMRole</span><span class="sxs-lookup"><span data-stu-id="7ebf0-139">-VMRole</span></span>
<span data-ttu-id="7ebf0-140">Sanal makine rolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-140">Specifies a virtual machine role.</span></span>
<span data-ttu-id="7ebf0-141">Sanal makine rolünü almak için **Get-WAPackVMRole** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-141">To get a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebf0-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ebf0-142">-Confirm</span></span>
<span data-ttu-id="7ebf0-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ebf0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ebf0-144">-WhatIf</span></span>
<span data-ttu-id="7ebf0-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ebf0-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ebf0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebf0-147">CommonParameters</span></span>
<span data-ttu-id="7ebf0-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ebf0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebf0-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ebf0-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebf0-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ebf0-150">INPUTS</span></span>

## <span data-ttu-id="7ebf0-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ebf0-151">OUTPUTS</span></span>

## <span data-ttu-id="7ebf0-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ebf0-152">NOTES</span></span>

## <span data-ttu-id="7ebf0-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ebf0-153">RELATED LINKS</span></span>

[<span data-ttu-id="7ebf0-154">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7ebf0-154">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="7ebf0-155">Yeni-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7ebf0-155">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="7ebf0-156">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7ebf0-156">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


