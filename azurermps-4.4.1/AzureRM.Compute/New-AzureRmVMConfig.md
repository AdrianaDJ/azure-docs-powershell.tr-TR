---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 2022a8a830d868f412e505f23e65c4c297bea543
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594785"
---
# <span data-ttu-id="05286-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="05286-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="05286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05286-102">SYNOPSIS</span></span>
<span data-ttu-id="05286-103">Yapılandırılabilir bir sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05286-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05286-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05286-104">SYNTAX</span></span>

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [[-IdentityType] <ResourceIdentityType>] [-AssignIdentity] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05286-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="05286-105">DESCRIPTION</span></span>
<span data-ttu-id="05286-106">**Yeni-AzureRmVMConfig** cmdlet 'i Azure için yapılandırılabilir bir yerel sanal makine nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05286-106">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="05286-107">Diğer cmdlet 'ler, set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-Azurermvmnetworkınterface ve set-Azurermvmosdısk gibi bir sanal makine nesnesini yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="05286-107">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="05286-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05286-108">EXAMPLES</span></span>

### <span data-ttu-id="05286-109">Örnek 1: sanal makine nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="05286-109">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="05286-110">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="05286-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="05286-111">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="05286-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="05286-112">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="05286-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="05286-113">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="05286-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="05286-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05286-114">PARAMETERS</span></span>

### <span data-ttu-id="05286-115">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="05286-115">-AssignIdentity</span></span>
<span data-ttu-id="05286-116">Sanal makine için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="05286-116">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05286-117">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="05286-117">-AvailabilitySetId</span></span>
<span data-ttu-id="05286-118">Bir kullanılabilirlik kümesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="05286-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="05286-119">Bir kullanılabilirlik kümesi nesnesi edinmek için Get-AzureRmAvailabilitySet cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="05286-119">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="05286-120">Kullanılabilirlik kümesi nesnesi bir KIMLIK içeriyor.</span><span class="sxs-lookup"><span data-stu-id="05286-120">The availability set object contains an ID property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05286-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05286-121">-DefaultProfile</span></span>
<span data-ttu-id="05286-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05286-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05286-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="05286-123">-IdentityType</span></span>
<span data-ttu-id="05286-124">Yapılandırılmış sanal makinenin kimliği.</span><span class="sxs-lookup"><span data-stu-id="05286-124">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05286-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="05286-125">-LicenseType</span></span>
<span data-ttu-id="05286-126">Kendi lisans senaryonuzu veren lisans türü.</span><span class="sxs-lookup"><span data-stu-id="05286-126">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05286-127">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="05286-127">-Tags</span></span>
<span data-ttu-id="05286-128">Kaynağa iliştirilmiş etiketler.</span><span class="sxs-lookup"><span data-stu-id="05286-128">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05286-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="05286-129">-VMName</span></span>
<span data-ttu-id="05286-130">Sanal makine için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="05286-130">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05286-131">-VMSize</span><span class="sxs-lookup"><span data-stu-id="05286-131">-VMSize</span></span>
<span data-ttu-id="05286-132">Sanal makinenin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="05286-132">Specifies the size for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05286-133">-Bölge</span><span class="sxs-lookup"><span data-stu-id="05286-133">-Zone</span></span>
<span data-ttu-id="05286-134">Sanal makinenin bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05286-134">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05286-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05286-135">CommonParameters</span></span>
<span data-ttu-id="05286-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05286-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05286-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05286-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05286-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05286-138">INPUTS</span></span>

## <span data-ttu-id="05286-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05286-139">OUTPUTS</span></span>

## <span data-ttu-id="05286-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05286-140">NOTES</span></span>

## <span data-ttu-id="05286-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05286-141">RELATED LINKS</span></span>

[<span data-ttu-id="05286-142">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="05286-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="05286-143">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="05286-143">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="05286-144">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="05286-144">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="05286-145">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="05286-145">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


