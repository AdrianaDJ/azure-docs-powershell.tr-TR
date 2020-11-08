---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 83D18A17-94A4-4FB8-9DA6-F652D5BB84C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf06561ac5f8c9e0c19edb88b7a8ff5ef816c609
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105886"
---
# <span data-ttu-id="cadcf-101">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="cadcf-101">New-WAPackVMSubnet</span></span>

## <span data-ttu-id="cadcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cadcf-102">SYNOPSIS</span></span>
<span data-ttu-id="cadcf-103">Sanal makine alt ağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cadcf-103">Creates a virtual machine subnet.</span></span>

## <span data-ttu-id="cadcf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cadcf-104">SYNTAX</span></span>

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="cadcf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cadcf-105">DESCRIPTION</span></span>
<span data-ttu-id="cadcf-106">**Yeni-WAPackVMSubnet** cmdlet 'i sanal makine alt ağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cadcf-106">The **New-WAPackVMSubnet** cmdlet creates a virtual machine subnet.</span></span>

## <span data-ttu-id="cadcf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cadcf-107">EXAMPLES</span></span>

### <span data-ttu-id="cadcf-108">Örnek 1: sanal makine alt ağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="cadcf-108">Example 1: Create a virtual machine subnet</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

<span data-ttu-id="cadcf-109">İlk komut öncelikle, yeni sanal makine alt ağı eklemek istediğimiz sanal makine ağını alır.</span><span class="sxs-lookup"><span data-stu-id="cadcf-109">The first command first retrieves the virtual machine network to which we want to add a new virtual machine subnet.</span></span>
<span data-ttu-id="cadcf-110">Bu sanal makine ağının adı ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="cadcf-110">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="cadcf-111">İkinci komut, daha önce alma sanal makine ağını, bir ad ContosoVMSubnet01 ve 192.168.1.0/24 ağını kullanarak sanal makine alt ağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cadcf-111">The second command creates a virtual machine subnet using the previously retrieve virtual machine network, a name ContosoVMSubnet01 and a subnet 192.168.1.0/24.</span></span>

## <span data-ttu-id="cadcf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cadcf-112">PARAMETERS</span></span>

### <span data-ttu-id="cadcf-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="cadcf-113">-Name</span></span>
<span data-ttu-id="cadcf-114">Sanal makine alt ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cadcf-114">Specifies a name for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="cadcf-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="cadcf-115">-Profile</span></span>
<span data-ttu-id="cadcf-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cadcf-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cadcf-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="cadcf-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cadcf-118">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="cadcf-118">-Subnet</span></span>
<span data-ttu-id="cadcf-119">Sanal makine alt ağının alt ağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cadcf-119">Specifies a subnet for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="cadcf-120">-VNet</span><span class="sxs-lookup"><span data-stu-id="cadcf-120">-VNet</span></span>
<span data-ttu-id="cadcf-121">Sanal makine alt ağıyla ilişkili bir VNet belirtir.</span><span class="sxs-lookup"><span data-stu-id="cadcf-121">Specifies a VNet associated with the virtual machine subnet.</span></span>

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

### <span data-ttu-id="cadcf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadcf-122">CommonParameters</span></span>
<span data-ttu-id="cadcf-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cadcf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadcf-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cadcf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadcf-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cadcf-125">INPUTS</span></span>

## <span data-ttu-id="cadcf-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cadcf-126">OUTPUTS</span></span>

## <span data-ttu-id="cadcf-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cadcf-127">NOTES</span></span>

## <span data-ttu-id="cadcf-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cadcf-128">RELATED LINKS</span></span>

[<span data-ttu-id="cadcf-129">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="cadcf-129">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="cadcf-130">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="cadcf-130">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="cadcf-131">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="cadcf-131">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


