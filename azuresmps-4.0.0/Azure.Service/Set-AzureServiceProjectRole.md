---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105952"
---
# <span data-ttu-id="6c3d2-101">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="6c3d2-101">Set-AzureServiceProjectRole</span></span>

## <span data-ttu-id="6c3d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="6c3d2-103">Bir rolün örnek sayısını veya çalışma zamanı sürümünü ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-103">Sets the number of instances or the runtime version of a role.</span></span>

## <span data-ttu-id="6c3d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c3d2-104">SYNTAX</span></span>

### <span data-ttu-id="6c3d2-105">Kopyalarına</span><span class="sxs-lookup"><span data-stu-id="6c3d2-105">Instances</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c3d2-106">Zamaný</span><span class="sxs-lookup"><span data-stu-id="6c3d2-106">Runtime</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6c3d2-107">VMSize</span><span class="sxs-lookup"><span data-stu-id="6c3d2-107">VMSize</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c3d2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c3d2-108">DESCRIPTION</span></span>
<span data-ttu-id="6c3d2-109">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6c3d2-110">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6c3d2-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6c3d2-111">**Set-AzureServiceProjectRole** cmdlet 'i belirtilen rolün rol örneklerinin sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-111">The **Set-AzureServiceProjectRole** cmdlet sets the number of role instances for the specified role.</span></span>

## <span data-ttu-id="6c3d2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c3d2-112">EXAMPLES</span></span>

### <span data-ttu-id="6c3d2-113">Örnek 1: Web rolü için örnekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="6c3d2-113">Example 1: Set instances for a web role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

<span data-ttu-id="6c3d2-114">MyWebRole1 adlı web rolü için örnek sayısını 2 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-114">Sets the number of instances for the web role named MyWebRole1 to 2.</span></span>

### <span data-ttu-id="6c3d2-115">Örnek 2: çalışan rolü için örnekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="6c3d2-115">Example 2: Set instances for a worker role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

<span data-ttu-id="6c3d2-116">WorkerRole1 adlı çalışan rolünün rol örneği sayımını 2 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-116">Sets the role instance count for the worker role named WorkerRole1 to 2.</span></span>

### <span data-ttu-id="6c3d2-117">Örnek 3: rol hizmeti için çalışma zamanı sürümünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="6c3d2-117">Example 3: Set the runtime version for a role service</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

<span data-ttu-id="6c3d2-118">MyRole1 için node.exe çalıştırma zamanı sürümünü 0.6.20 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-118">Sets the node.exe runtime version for role MyRole1 to 0.6.20.</span></span>

## <span data-ttu-id="6c3d2-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c3d2-119">PARAMETERS</span></span>

### <span data-ttu-id="6c3d2-120">-Örnekler</span><span class="sxs-lookup"><span data-stu-id="6c3d2-120">-Instances</span></span>
<span data-ttu-id="6c3d2-121">Belirtilen Web veya alt rolün rol örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-121">Specifies the number of role instances for the specified web or worker role.</span></span>

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c3d2-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6c3d2-122">-PassThru</span></span>
<span data-ttu-id="6c3d2-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6c3d2-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6c3d2-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="6c3d2-125">-Profile</span></span>
<span data-ttu-id="6c3d2-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c3d2-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c3d2-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="6c3d2-128">-RoleName</span></span>
<span data-ttu-id="6c3d2-129">Değiştirilecek Web veya işçi rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-129">Specifies the name of the web or worker role to be changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c3d2-130">-Runtime</span><span class="sxs-lookup"><span data-stu-id="6c3d2-130">-Runtime</span></span>
<span data-ttu-id="6c3d2-131">Belirtilen role eklenecek çalışma zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-131">Specifies the runtime to add to the specified role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c3d2-132">-Version</span><span class="sxs-lookup"><span data-stu-id="6c3d2-132">-Version</span></span>
<span data-ttu-id="6c3d2-133">Role eklenecek çalışma zamanının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-133">Specifies the version of the runtime to add to the role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c3d2-134">-VMSize</span><span class="sxs-lookup"><span data-stu-id="6c3d2-134">-VMSize</span></span>
<span data-ttu-id="6c3d2-135">Rolün sanal makine boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-135">Specifies the virtual machine size of the role.</span></span>

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c3d2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c3d2-136">CommonParameters</span></span>
<span data-ttu-id="6c3d2-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c3d2-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c3d2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c3d2-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c3d2-139">INPUTS</span></span>

###  
<span data-ttu-id="6c3d2-140">Sanal makinenin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c3d2-140">Specifies the size of the virtual machine.</span></span>

## <span data-ttu-id="6c3d2-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c3d2-141">OUTPUTS</span></span>

## <span data-ttu-id="6c3d2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c3d2-142">NOTES</span></span>

## <span data-ttu-id="6c3d2-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c3d2-143">RELATED LINKS</span></span>

[<span data-ttu-id="6c3d2-144">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="6c3d2-144">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


