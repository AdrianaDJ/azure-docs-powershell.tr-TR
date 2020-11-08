---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 73CEA6A8-46C9-4772-9A67-03F532696CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1287b3a0bb1cc39dea78fb4e92d2dcc4508c6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105543"
---
# <span data-ttu-id="279d9-101">Get-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="279d9-101">Get-AzureSubnet</span></span>

## <span data-ttu-id="279d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="279d9-102">SYNOPSIS</span></span>
<span data-ttu-id="279d9-103">Belirtilen Azure sanal makinesiyle ilişkili alt ağların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="279d9-103">Gets a list of subnets associated with the specified Azure virtual machine.</span></span>

## <span data-ttu-id="279d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="279d9-104">SYNTAX</span></span>

```
Get-AzureSubnet -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="279d9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="279d9-105">DESCRIPTION</span></span>
<span data-ttu-id="279d9-106">**Get-azuyeniden PNet** cmdlet 'i belirtilen sanal makineyle ilişkili alt ağları listeler.</span><span class="sxs-lookup"><span data-stu-id="279d9-106">The **Get-AzureSubnet** cmdlet returns a list the subnets associated with the specified virtual machine.</span></span>
<span data-ttu-id="279d9-107">Sanal makineyi belirtmek için **Get-AzureVM** kullanın.</span><span class="sxs-lookup"><span data-stu-id="279d9-107">Use **Get-AzureVM** to specify the virtual machine.</span></span>

## <span data-ttu-id="279d9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="279d9-108">EXAMPLES</span></span>

### <span data-ttu-id="279d9-109">Örnek 1: sanal makinenin alt ağlarını alma</span><span class="sxs-lookup"><span data-stu-id="279d9-109">Example 1: Get subnets for a virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine01"
C:\PS> Get-AzureSubnet -VM $VM
```

<span data-ttu-id="279d9-110">İlk komut, ContosoService03 adındaki hizmette VirtualMachine01 adlı bir sanal makine alır ve $VM değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="279d9-110">The first command gets a virtual machine named VirtualMachine01 in the service named ContosoService03, and then stores it in the $VM variable.</span></span>

<span data-ttu-id="279d9-111">İkinci komut $VM sanal makinesi için Azure alt ağlarını alır.</span><span class="sxs-lookup"><span data-stu-id="279d9-111">The second command gets the Azure subnets for the virtual machine in $VM.</span></span>

## <span data-ttu-id="279d9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="279d9-112">PARAMETERS</span></span>

### <span data-ttu-id="279d9-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="279d9-113">-InformationAction</span></span>
<span data-ttu-id="279d9-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="279d9-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="279d9-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="279d9-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="279d9-116">'A</span><span class="sxs-lookup"><span data-stu-id="279d9-116">Continue</span></span>
- <span data-ttu-id="279d9-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="279d9-117">Ignore</span></span>
- <span data-ttu-id="279d9-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="279d9-118">Inquire</span></span>
- <span data-ttu-id="279d9-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="279d9-119">SilentlyContinue</span></span>
- <span data-ttu-id="279d9-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="279d9-120">Stop</span></span>
- <span data-ttu-id="279d9-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="279d9-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279d9-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="279d9-122">-InformationVariable</span></span>
<span data-ttu-id="279d9-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="279d9-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279d9-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="279d9-124">-Profile</span></span>
<span data-ttu-id="279d9-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="279d9-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="279d9-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="279d9-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="279d9-127">-VM</span><span class="sxs-lookup"><span data-stu-id="279d9-127">-VM</span></span>
<span data-ttu-id="279d9-128">Alt ağ listesinin alınacağı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="279d9-128">Specifies the virtual machine object from which to get the subnet list.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="279d9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279d9-129">CommonParameters</span></span>
<span data-ttu-id="279d9-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="279d9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279d9-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="279d9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279d9-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="279d9-132">INPUTS</span></span>

## <span data-ttu-id="279d9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="279d9-133">OUTPUTS</span></span>

## <span data-ttu-id="279d9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="279d9-134">NOTES</span></span>

## <span data-ttu-id="279d9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="279d9-135">RELATED LINKS</span></span>

[<span data-ttu-id="279d9-136">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="279d9-136">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="279d9-137">Set-Azuyeniden gönderme</span><span class="sxs-lookup"><span data-stu-id="279d9-137">Set-AzureSubnet</span></span>](./Set-AzureSubnet.md)


