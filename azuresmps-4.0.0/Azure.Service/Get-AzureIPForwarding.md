---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BE661AC7-BA39-4D6A-8083-16CE9327DC08
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4c84155484435a9601af005393593040c9cfe4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106348"
---
# <span data-ttu-id="36914-101">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="36914-101">Get-AzureIPForwarding</span></span>

## <span data-ttu-id="36914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36914-102">SYNOPSIS</span></span>
<span data-ttu-id="36914-103">IP iletimi durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="36914-103">Gets the status of IP forwarding.</span></span>

## <span data-ttu-id="36914-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36914-104">SYNTAX</span></span>

### <span data-ttu-id="36914-105">Iaasıfpforwardingparamparam</span><span class="sxs-lookup"><span data-stu-id="36914-105">IaaSIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="36914-106">Slotıpforwardingparamset</span><span class="sxs-lookup"><span data-stu-id="36914-106">SlotIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="36914-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="36914-107">DESCRIPTION</span></span>
<span data-ttu-id="36914-108">**Get-AzureIPForwarding** CMDLET 'i IP iletimi durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="36914-108">The **Get-AzureIPForwarding** cmdlet gets the status of IP forwarding.</span></span>

## <span data-ttu-id="36914-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36914-109">EXAMPLES</span></span>

### <span data-ttu-id="36914-110">Örnek 1: sanal makine için IP iletme durumunu alma</span><span class="sxs-lookup"><span data-stu-id="36914-110">Example 1: Get IP forwarding status for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureIPForwarding
Disabled
```

<span data-ttu-id="36914-111">Bu komut, ContosoService adındaki hizmet için ContosoVM06 adındaki bir sanal makineyi alır ve bu sanal makine nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="36914-111">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="36914-112">Geçerli cmdlet, bu sanal makinenin IP iletimi durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="36914-112">The current cmdlet gets the status of IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="36914-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36914-113">PARAMETERS</span></span>

### <span data-ttu-id="36914-114">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="36914-114">-NetworkInterfaceName</span></span>
<span data-ttu-id="36914-115">Bu cmdlet 'in IP iletme durumunu aldığı ağ bağdaştırıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36914-115">Specifies the name of the network adapter for which this cmdlet gets IP forwarding status.</span></span>

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

### <span data-ttu-id="36914-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="36914-116">-Profile</span></span>
<span data-ttu-id="36914-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="36914-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="36914-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="36914-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="36914-119">-RoleName</span><span class="sxs-lookup"><span data-stu-id="36914-119">-RoleName</span></span>
<span data-ttu-id="36914-120">Bu cmdlet 'in IP iletme durumunu aldığı PaaS rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36914-120">Specifies the name of a PaaS role for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36914-121">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="36914-121">-ServiceName</span></span>
<span data-ttu-id="36914-122">Bulut hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36914-122">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="36914-123">PaaS rolü, bu parametrenin belirttiği hizmete aittir.</span><span class="sxs-lookup"><span data-stu-id="36914-123">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36914-124">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="36914-124">-Slot</span></span>
<span data-ttu-id="36914-125">PaaS yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36914-125">Specifies a PaaS slot.</span></span>
<span data-ttu-id="36914-126">Bu cmdlet 'in iletme durumunda olduğu PaaS rolünde bu parametrenin belirttiği yuva vardır.</span><span class="sxs-lookup"><span data-stu-id="36914-126">The PaaS role for which this cmdlet gets forwarding status has the slot that this parameter specifies.</span></span>
<span data-ttu-id="36914-127">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="36914-127">Valid values are:</span></span> 

- <span data-ttu-id="36914-128">Üretim</span><span class="sxs-lookup"><span data-stu-id="36914-128">Production</span></span>
- <span data-ttu-id="36914-129">Geçici saklama</span><span class="sxs-lookup"><span data-stu-id="36914-129">Staging</span></span> 

<span data-ttu-id="36914-130">Varsayılan değer Production değeridir.</span><span class="sxs-lookup"><span data-stu-id="36914-130">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36914-131">-VM</span><span class="sxs-lookup"><span data-stu-id="36914-131">-VM</span></span>
<span data-ttu-id="36914-132">Bu cmdlet 'in IP iletme durumunu aldığı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="36914-132">Specifies the virtual machine object for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36914-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36914-133">CommonParameters</span></span>
<span data-ttu-id="36914-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36914-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36914-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36914-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36914-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36914-136">INPUTS</span></span>

## <span data-ttu-id="36914-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36914-137">OUTPUTS</span></span>

### <span data-ttu-id="36914-138">System. String</span><span class="sxs-lookup"><span data-stu-id="36914-138">System.String</span></span>

## <span data-ttu-id="36914-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36914-139">NOTES</span></span>

## <span data-ttu-id="36914-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36914-140">RELATED LINKS</span></span>

[<span data-ttu-id="36914-141">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="36914-141">Set-AzureIPForwarding</span></span>](./Set-AzureIPForwarding.md)


