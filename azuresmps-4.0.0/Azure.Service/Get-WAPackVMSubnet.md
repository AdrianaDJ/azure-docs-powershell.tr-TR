---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0E358CEF-69E4-4639-918C-CE593E97B189
online version: ''
schema: 2.0.0
ms.openlocfilehash: d534a1734a49739db648558e8d7e62b22e43d561
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107355"
---
# <span data-ttu-id="f3e57-101">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="f3e57-101">Get-WAPackVMSubnet</span></span>

## <span data-ttu-id="f3e57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3e57-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e57-103">Sanal makine alt ağ nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="f3e57-103">Gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="f3e57-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3e57-104">SYNTAX</span></span>

### <span data-ttu-id="f3e57-105">FromVMNetworkObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f3e57-105">FromVMNetworkObject (Default)</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f3e57-106">FromName</span><span class="sxs-lookup"><span data-stu-id="f3e57-106">FromName</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f3e57-107">FromId</span><span class="sxs-lookup"><span data-stu-id="f3e57-107">FromId</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f3e57-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3e57-108">DESCRIPTION</span></span>
<span data-ttu-id="f3e57-109">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="f3e57-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="f3e57-110">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f3e57-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f3e57-111">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f3e57-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f3e57-112">**Get-WAPackVMSubnet** cmdlet 'i sanal makine alt ağ nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="f3e57-112">The **Get-WAPackVMSubnet** cmdlet gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="f3e57-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3e57-113">EXAMPLES</span></span>

### <span data-ttu-id="f3e57-114">Örnek 1: ad kullanarak sanal makine alt ağını alma</span><span class="sxs-lookup"><span data-stu-id="f3e57-114">Example 1: Get a virtual machine subnet by using a name</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMTemplate -VNet $VNet -Name "ContosoSubnet01"
```

<span data-ttu-id="f3e57-115">Bu komut, ContosoSubnet01 adındaki sanal makine alt ağını alır.</span><span class="sxs-lookup"><span data-stu-id="f3e57-115">This command gets the virtual machine subnet named ContosoSubnet01.</span></span>

### <span data-ttu-id="f3e57-116">Örnek 2: KIMLIK kullanarak sanal makine alt ağını alma</span><span class="sxs-lookup"><span data-stu-id="f3e57-116">Example 2: Get a virtual machine subnet by using an ID</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="f3e57-117">Bu komut, belirtilen KIMLIĞE sahip sanal makine alt ağını alır.</span><span class="sxs-lookup"><span data-stu-id="f3e57-117">This command gets the virtual machine subnet that has the specified ID.</span></span>

### <span data-ttu-id="f3e57-118">Örnek 3: verilen sanallaştırılmış ağlardan tüm sanal makine alt ağlarını alma</span><span class="sxs-lookup"><span data-stu-id="f3e57-118">Example 3: Get all virtual machine subnets from a given virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet
```

<span data-ttu-id="f3e57-119">Bu komut, belirli bir sanallaştırılmış ağın tüm sanal makine alt ağlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f3e57-119">This command gets all the virtual machine subnets from a given virtualized network.</span></span>

## <span data-ttu-id="f3e57-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3e57-120">PARAMETERS</span></span>

### <span data-ttu-id="f3e57-121">-ID</span><span class="sxs-lookup"><span data-stu-id="f3e57-121">-ID</span></span>
<span data-ttu-id="f3e57-122">Sanal makine alt ağının benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3e57-122">Specifies the unique ID of a virtual machine subnet.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e57-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="f3e57-123">-Name</span></span>
<span data-ttu-id="f3e57-124">Sanal makine alt ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3e57-124">Specifies the name of a virtual machine subnet.</span></span>

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

### <span data-ttu-id="f3e57-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="f3e57-125">-Profile</span></span>
<span data-ttu-id="f3e57-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3e57-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3e57-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f3e57-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3e57-128">-VNet</span><span class="sxs-lookup"><span data-stu-id="f3e57-128">-VNet</span></span>
<span data-ttu-id="f3e57-129">Sanal makine alt ağıyla ilişkili VNet belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3e57-129">Specifies the VNet associated with a virtual machine subnet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e57-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e57-130">CommonParameters</span></span>
<span data-ttu-id="f3e57-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3e57-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e57-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3e57-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e57-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3e57-133">INPUTS</span></span>

## <span data-ttu-id="f3e57-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3e57-134">OUTPUTS</span></span>

## <span data-ttu-id="f3e57-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3e57-135">NOTES</span></span>

## <span data-ttu-id="f3e57-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3e57-136">RELATED LINKS</span></span>

[<span data-ttu-id="f3e57-137">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="f3e57-137">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="f3e57-138">Yeni-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="f3e57-138">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)

[<span data-ttu-id="f3e57-139">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="f3e57-139">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


