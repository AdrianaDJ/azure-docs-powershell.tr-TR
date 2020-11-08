---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107381"
---
# <span data-ttu-id="7cb6d-101">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="7cb6d-101">New-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="7cb6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cb6d-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb6d-103">Statik IP adresi havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-103">Creates a static IP address pool.</span></span>

## <span data-ttu-id="7cb6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7cb6d-104">SYNTAX</span></span>

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7cb6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7cb6d-105">DESCRIPTION</span></span>
<span data-ttu-id="7cb6d-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7cb6d-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7cb6d-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7cb6d-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7cb6d-109">**Yeni-Wapackstaticıpaddresspool** cmdlet 'ı statik IP adresi havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-109">The **New-WAPackStaticIPAddressPool** cmdlet creates a static IP address pool.</span></span>

## <span data-ttu-id="7cb6d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7cb6d-110">EXAMPLES</span></span>

### <span data-ttu-id="7cb6d-111">Örnek 1: statik IP adresi havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="7cb6d-111">Example 1: Create a static IP address pool</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

<span data-ttu-id="7cb6d-112">İlk komut öncelikle, statik IP adresi havuzu eklemek istediğimiz sanal makine ağını alır.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-112">The first command first retrieves the virtual machine network to which we want to add the static IP address pool.</span></span>
<span data-ttu-id="7cb6d-113">Bu sanal makine ağının adı ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-113">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="7cb6d-114">İkinci komut, statik IP adresi havuzunu eklemek istediğimiz ContosoVMSubnet01 adlı sanal makine alt ağını almak için daha önce alınan sanal makine ağını kullanır.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-114">The second command uses the previously retrieved virtual machine network to get the virtual machine subnet named ContosoVMSubnet01 to which we want to add the static IP address pool.</span></span>

<span data-ttu-id="7cb6d-115">Son komut, ad ContosoStaticIpAddressPool01 ile yeni bir statik IP adresi havuzu oluşturur ve bir aralığı Başlat 192.168.1.0 ve bir Aralık uç 192.168.1.10.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-115">The last command creates a new static IP address pool with a name ContosoStaticIpAddressPool01 and a range start 192.168.1.0 and a range end 192.168.1.10.</span></span>

## <span data-ttu-id="7cb6d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7cb6d-116">PARAMETERS</span></span>

### <span data-ttu-id="7cb6d-117">-IPAddressRangeEnd</span><span class="sxs-lookup"><span data-stu-id="7cb6d-117">-IPAddressRangeEnd</span></span>
<span data-ttu-id="7cb6d-118">Statik IP adresi havuzu için bir IP adresi aralığı sonu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-118">Specifies an IP address range end for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb6d-119">-Ipaddressrangestart</span><span class="sxs-lookup"><span data-stu-id="7cb6d-119">-IPAddressRangeStart</span></span>
<span data-ttu-id="7cb6d-120">Statik IP adresi havuzu için bir IP adresi aralığı başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-120">Specifies an IP address range start for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb6d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="7cb6d-121">-Name</span></span>
<span data-ttu-id="7cb6d-122">Statik IP adresi havuzu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-122">Specifies a name for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb6d-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="7cb6d-123">-Profile</span></span>
<span data-ttu-id="7cb6d-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7cb6d-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7cb6d-126">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="7cb6d-126">-VMSubnet</span></span>
<span data-ttu-id="7cb6d-127">Statik IP adresi havuzuyla ilişkili bir VMSubnet belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-127">Specifies a VMSubnet associated with the static IP address pool.</span></span>

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

### <span data-ttu-id="7cb6d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb6d-128">CommonParameters</span></span>
<span data-ttu-id="7cb6d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb6d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cb6d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb6d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7cb6d-131">INPUTS</span></span>

## <span data-ttu-id="7cb6d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7cb6d-132">OUTPUTS</span></span>

## <span data-ttu-id="7cb6d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7cb6d-133">NOTES</span></span>

## <span data-ttu-id="7cb6d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7cb6d-134">RELATED LINKS</span></span>

[<span data-ttu-id="7cb6d-135">Get-Wapackstaticıpaddresspool</span><span class="sxs-lookup"><span data-stu-id="7cb6d-135">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="7cb6d-136">Remove-Wapackstaticıpaddresspool</span><span class="sxs-lookup"><span data-stu-id="7cb6d-136">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


