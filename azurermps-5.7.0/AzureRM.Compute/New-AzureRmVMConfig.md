---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 45cb93e652f9c1524ef1bb11972f184336ef7328
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762752"
---
# <span data-ttu-id="4203a-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="4203a-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="4203a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4203a-102">SYNOPSIS</span></span>
<span data-ttu-id="4203a-103">Yapılandırılabilir bir sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4203a-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4203a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4203a-104">SYNTAX</span></span>

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [-LicenseType <String>] [-IdentityType <ResourceIdentityType>] [-Tags <Hashtable>] [<CommonParameters>]
```

## <span data-ttu-id="4203a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4203a-105">DESCRIPTION</span></span>
<span data-ttu-id="4203a-106">**Yeni-AzureRmVMConfig** cmdlet 'i Azure için yapılandırılabilir bir yerel sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4203a-106">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="4203a-107">Diğer cmdlet 'ler, set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-Azurermvmnetworkınterface ve set-Azurermvmosdısk gibi bir sanal makine nesnesini yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4203a-107">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="4203a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4203a-108">EXAMPLES</span></span>

### <span data-ttu-id="4203a-109">Örnek 1: sanal makine nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4203a-109">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="4203a-110">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4203a-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="4203a-111">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4203a-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4203a-112">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="4203a-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4203a-113">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="4203a-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="4203a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4203a-114">PARAMETERS</span></span>

### <span data-ttu-id="4203a-115">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="4203a-115">-AvailabilitySetId</span></span>
<span data-ttu-id="4203a-116">Bir kullanılabilirlik kümesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4203a-116">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="4203a-117">Bir kullanılabilirlik kümesi nesnesi edinmek için Get-AzureRmAvailabilitySet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4203a-117">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="4203a-118">Kullanılabilirlik kümesi nesnesi bir KIMLIK içeriyor.</span><span class="sxs-lookup"><span data-stu-id="4203a-118">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4203a-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4203a-119">-IdentityType</span></span>
<span data-ttu-id="4203a-120">Yapılandırılmış sanal makinenin kimliği.</span><span class="sxs-lookup"><span data-stu-id="4203a-120">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4203a-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4203a-121">-LicenseType</span></span>
<span data-ttu-id="4203a-122">Kendi lisans senaryonuzu veren lisans türü.</span><span class="sxs-lookup"><span data-stu-id="4203a-122">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4203a-123">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="4203a-123">-Tags</span></span>
<span data-ttu-id="4203a-124">Kaynağa iliştirilmiş etiketler.</span><span class="sxs-lookup"><span data-stu-id="4203a-124">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4203a-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="4203a-125">-VMName</span></span>
<span data-ttu-id="4203a-126">Sanal makine için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="4203a-126">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4203a-127">-VMSize</span><span class="sxs-lookup"><span data-stu-id="4203a-127">-VMSize</span></span>
<span data-ttu-id="4203a-128">Sanal makinenin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4203a-128">Specifies the size for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4203a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4203a-129">CommonParameters</span></span>
<span data-ttu-id="4203a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4203a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4203a-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4203a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4203a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4203a-132">INPUTS</span></span>

### <span data-ttu-id="4203a-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4203a-133">None</span></span>
<span data-ttu-id="4203a-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4203a-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4203a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4203a-135">OUTPUTS</span></span>

## <span data-ttu-id="4203a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4203a-136">NOTES</span></span>

## <span data-ttu-id="4203a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4203a-137">RELATED LINKS</span></span>

[<span data-ttu-id="4203a-138">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4203a-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="4203a-139">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4203a-139">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="4203a-140">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="4203a-140">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="4203a-141">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4203a-141">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


