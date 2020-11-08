---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E54E4D16-DB2A-4626-B543-773C187B2E08
online version: ''
schema: 2.0.0
ms.openlocfilehash: d242418117b1bb576206f9ebb5fd568bd3e63cd1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105862"
---
# <span data-ttu-id="19357-101">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="19357-101">Set-AzureStaticVNetIP</span></span>

## <span data-ttu-id="19357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19357-102">SYNOPSIS</span></span>
<span data-ttu-id="19357-103">Sanal makine nesnesinin statik VNet IP adresi bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="19357-103">Sets the static VNet IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="19357-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19357-104">SYNTAX</span></span>

```
Set-AzureStaticVNetIP [-IPAddress] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="19357-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19357-105">DESCRIPTION</span></span>
<span data-ttu-id="19357-106">**Set-AzureStaticVNetIP** cmdlet 'i, sanal makine nesnesinin statik sanal ağ (VNet) IP adresi bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="19357-106">The **Set-AzureStaticVNetIP** cmdlet sets the static virtual network (VNet) IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="19357-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19357-107">EXAMPLES</span></span>

### <span data-ttu-id="19357-108">Örnek 1: sanal makineyle ilişkili sanal ağ IP adresini ayarlama</span><span class="sxs-lookup"><span data-stu-id="19357-108">Example 1: Set the virtual network IP address associated with a virtual machine</span></span>
```
PS C:\> # Prerequisite: VNet has been set up with SubNet
          # Set-AzureVNetConfig -ConfigurationPath $vnetConfigPath;

          $vm = New-AzureVMConfig -Name $vmname -ImageName $img -InstanceSize $sz | Add-AzureProvisioningConfig -Windows -Password $pwd -AdminUsername $usr;
          $vm = Set-AzureSubNet -VM $vm -SubNetNames $sn;
          Set-AzureStaticVNetIP -IPAddress $ip -VM $vm;
          New-AzureVM -ServiceName $svc -VMs $vm -VNetName $vnetName -Location $loc;
```

<span data-ttu-id="19357-109">İlk komut sanal ağın yapılandırma yolunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="19357-109">The first command sets the configuration path for a virtual network.</span></span>

<span data-ttu-id="19357-110">İkinci komut bir sanal makine yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19357-110">The second command creates a virtual machine configuration.</span></span>

<span data-ttu-id="19357-111">Üçüncü komut sanal makinenin alt ağını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="19357-111">The third command sets the subnet for the virtual machine.</span></span>

<span data-ttu-id="19357-112">Dördüncü komut sanal makinenin IP adresini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="19357-112">The fourth command sets the IP address for the virtual machine.</span></span>

<span data-ttu-id="19357-113">Beşinci komut sanal makineyi kullanarak sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19357-113">The fifth command creates a virtual machine using the virtual machine.</span></span>

## <span data-ttu-id="19357-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19357-114">PARAMETERS</span></span>

### <span data-ttu-id="19357-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="19357-115">-InformationAction</span></span>
<span data-ttu-id="19357-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19357-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="19357-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="19357-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19357-118">'A</span><span class="sxs-lookup"><span data-stu-id="19357-118">Continue</span></span>
- <span data-ttu-id="19357-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="19357-119">Ignore</span></span>
- <span data-ttu-id="19357-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="19357-120">Inquire</span></span>
- <span data-ttu-id="19357-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="19357-121">SilentlyContinue</span></span>
- <span data-ttu-id="19357-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="19357-122">Stop</span></span>
- <span data-ttu-id="19357-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="19357-123">Suspend</span></span>

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

### <span data-ttu-id="19357-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="19357-124">-InformationVariable</span></span>
<span data-ttu-id="19357-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="19357-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="19357-126">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="19357-126">-IPAddress</span></span>
<span data-ttu-id="19357-127">Statik VNet IP adresini belirtir</span><span class="sxs-lookup"><span data-stu-id="19357-127">Specifies the static VNet IP address</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19357-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="19357-128">-Profile</span></span>
<span data-ttu-id="19357-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19357-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19357-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="19357-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19357-131">-VM</span><span class="sxs-lookup"><span data-stu-id="19357-131">-VM</span></span>
<span data-ttu-id="19357-132">Statik VNet IP adresini ayarlanacak kalıcı bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19357-132">Specifies a persistent virtual machine object for which to set the static VNet IP address.</span></span>

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

### <span data-ttu-id="19357-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19357-133">CommonParameters</span></span>
<span data-ttu-id="19357-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19357-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19357-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19357-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19357-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19357-136">INPUTS</span></span>

## <span data-ttu-id="19357-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19357-137">OUTPUTS</span></span>

## <span data-ttu-id="19357-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19357-138">NOTES</span></span>

## <span data-ttu-id="19357-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19357-139">RELATED LINKS</span></span>

[<span data-ttu-id="19357-140">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="19357-140">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="19357-141">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="19357-141">Test-AzureStaticVNetIP</span></span>](./Test-AzureStaticVNetIP.md)


