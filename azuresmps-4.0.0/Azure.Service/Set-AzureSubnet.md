---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 69974370-4542-4417-BD9D-3928EB005C31
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81d6e523978196a47b01d21aa8e857027b0b4f40
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105951"
---
# <span data-ttu-id="fabd7-101">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="fabd7-101">Set-AzureSubnet</span></span>

## <span data-ttu-id="fabd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fabd7-102">SYNOPSIS</span></span>
<span data-ttu-id="fabd7-103">Bir Azure sanal makinesinin alt ağ listesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fabd7-103">Defines the subnet list for an Azure virtual machine.</span></span>

## <span data-ttu-id="fabd7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fabd7-104">SYNTAX</span></span>

```
Set-AzureSubnet [-SubnetNames] <String[]> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fabd7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fabd7-105">DESCRIPTION</span></span>
<span data-ttu-id="fabd7-106">**Set-azuyeniden PNet** cmdlet 'i sanal makine yapılandırması için alt ağ listesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fabd7-106">The **Set-AzureSubnet** cmdlet sets the subnet list for a virtual machine configuration.</span></span>
<span data-ttu-id="fabd7-107">Bir sanal makinenin alt ağlarını ayarlamak için **New-AzureVM** ile kullanın.</span><span class="sxs-lookup"><span data-stu-id="fabd7-107">Use with **New-AzureVM** to set the subnets for a virtual machine.</span></span>

## <span data-ttu-id="fabd7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fabd7-108">EXAMPLES</span></span>

### <span data-ttu-id="fabd7-109">Örnek 1: sanal makine yapılandırmasına alt ağ ekleme</span><span class="sxs-lookup"><span data-stu-id="fabd7-109">Example 1: Add a subnet to a virtual machine configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine04" -ImageName $image -InstanceSize "Small" | Add-AzureProvisioningConfig -Windows -Password "password" | Set-AzureSubnet "PubSubnet","PrivSubnet" | New-AzureVM -ServiceName "ContosoService03"
```

<span data-ttu-id="fabd7-110">Bu komut sanal makine yapılandırmasına bir alt ağ ekler ve VirtualMachine04 adlı sanal makineyi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fabd7-110">This command adds a subnet to the virtual machine configuration, and then creates the virtual machine named VirtualMachine04.</span></span>

## <span data-ttu-id="fabd7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fabd7-111">PARAMETERS</span></span>

### <span data-ttu-id="fabd7-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fabd7-112">-InformationAction</span></span>
<span data-ttu-id="fabd7-113">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fabd7-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fabd7-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fabd7-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fabd7-115">'A</span><span class="sxs-lookup"><span data-stu-id="fabd7-115">Continue</span></span>
- <span data-ttu-id="fabd7-116">Manıza</span><span class="sxs-lookup"><span data-stu-id="fabd7-116">Ignore</span></span>
- <span data-ttu-id="fabd7-117">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fabd7-117">Inquire</span></span>
- <span data-ttu-id="fabd7-118">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fabd7-118">SilentlyContinue</span></span>
- <span data-ttu-id="fabd7-119">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fabd7-119">Stop</span></span>
- <span data-ttu-id="fabd7-120">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fabd7-120">Suspend</span></span>

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

### <span data-ttu-id="fabd7-121">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fabd7-121">-InformationVariable</span></span>
<span data-ttu-id="fabd7-122">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fabd7-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fabd7-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="fabd7-123">-Profile</span></span>
<span data-ttu-id="fabd7-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fabd7-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fabd7-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fabd7-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fabd7-126">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="fabd7-126">-SubnetNames</span></span>
<span data-ttu-id="fabd7-127">Alt ağ adları listesini içeren bir dizi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fabd7-127">Specifies an array that contains the list of subnet names.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fabd7-128">-VM</span><span class="sxs-lookup"><span data-stu-id="fabd7-128">-VM</span></span>
<span data-ttu-id="fabd7-129">Sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fabd7-129">Specifies the virtual machine object.</span></span>

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

### <span data-ttu-id="fabd7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabd7-130">CommonParameters</span></span>
<span data-ttu-id="fabd7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fabd7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabd7-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fabd7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabd7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fabd7-133">INPUTS</span></span>

## <span data-ttu-id="fabd7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fabd7-134">OUTPUTS</span></span>

## <span data-ttu-id="fabd7-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fabd7-135">NOTES</span></span>

## <span data-ttu-id="fabd7-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fabd7-136">RELATED LINKS</span></span>

[<span data-ttu-id="fabd7-137">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fabd7-137">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="fabd7-138">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fabd7-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="fabd7-139">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fabd7-139">Update-AzureVM</span></span>](./Update-AzureVM.md)


