---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4414EA89-8573-416E-A611-DA2135E350BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75b216b512c364a3285df185a3365b1fc85a3d94
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107431"
---
# <span data-ttu-id="323b5-101">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="323b5-101">Get-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="323b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="323b5-102">SYNOPSIS</span></span>
<span data-ttu-id="323b5-103">Statik IP adresi havuzu nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="323b5-103">Gets static IP address pool objects.</span></span>

## <span data-ttu-id="323b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="323b5-104">SYNTAX</span></span>

### <span data-ttu-id="323b5-105">FromVMSubnetObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="323b5-105">FromVMSubnetObject (Default)</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="323b5-106">FromName</span><span class="sxs-lookup"><span data-stu-id="323b5-106">FromName</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="323b5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="323b5-107">DESCRIPTION</span></span>
<span data-ttu-id="323b5-108">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="323b5-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="323b5-109">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="323b5-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="323b5-110">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="323b5-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="323b5-111">**Get-Wapackstaticıpaddresspool** cmdlet 'ı statik IP adresi havuzu nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="323b5-111">The **Get-WAPackStaticIPAddressPool** cmdlet gets static IP address pool objects.</span></span>

## <span data-ttu-id="323b5-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="323b5-112">EXAMPLES</span></span>

### <span data-ttu-id="323b5-113">Örnek 1: belirli bir VMSubnet 'den statik IP adresi havuzu alma</span><span class="sxs-lookup"><span data-stu-id="323b5-113">Example 1: Get a static IP address pool from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet -Name "ContosoStaticIPAddressPool01"
```

<span data-ttu-id="323b5-114">Bu komut, belirtilen bir VMSubnet 'den ContosoStaticIPAddressPool01 adındaki statik IP adresi havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="323b5-114">This command gets the static IP address pool named ContosoStaticIPAddressPool01 from a specified VMSubnet.</span></span>

### <span data-ttu-id="323b5-115">Örnek 2: belirli bir VMSubnet 'den tüm statik IP adresi havuzlarını alma</span><span class="sxs-lookup"><span data-stu-id="323b5-115">Example 2: Get all static IP address pools from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet
```

<span data-ttu-id="323b5-116">Bu komut belirtilen bir Vmsusonucunun tüm statik IP havuzlarını alır.</span><span class="sxs-lookup"><span data-stu-id="323b5-116">This command gets all the static IP pools from a specified VMSubet.</span></span>

## <span data-ttu-id="323b5-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="323b5-117">PARAMETERS</span></span>

### <span data-ttu-id="323b5-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="323b5-118">-Name</span></span>
<span data-ttu-id="323b5-119">Statik IP adresi havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="323b5-119">Specifies the name of a static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="323b5-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="323b5-120">-Profile</span></span>
<span data-ttu-id="323b5-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="323b5-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="323b5-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="323b5-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="323b5-123">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="323b5-123">-VMSubnet</span></span>
<span data-ttu-id="323b5-124">Statik IP adresi havuzuyla ilişkili **VMSubnet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="323b5-124">Specifies the **VMSubnet** object associated to the static IP address pool.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="323b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="323b5-125">CommonParameters</span></span>
<span data-ttu-id="323b5-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="323b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="323b5-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="323b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="323b5-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="323b5-128">INPUTS</span></span>

## <span data-ttu-id="323b5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="323b5-129">OUTPUTS</span></span>

## <span data-ttu-id="323b5-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="323b5-130">NOTES</span></span>

## <span data-ttu-id="323b5-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="323b5-131">RELATED LINKS</span></span>

[<span data-ttu-id="323b5-132">Yeni-Wapackstaticıpaddresspool</span><span class="sxs-lookup"><span data-stu-id="323b5-132">New-WAPackStaticIPAddressPool</span></span>](./New-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="323b5-133">Remove-Wapackstaticıpaddresspool</span><span class="sxs-lookup"><span data-stu-id="323b5-133">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


