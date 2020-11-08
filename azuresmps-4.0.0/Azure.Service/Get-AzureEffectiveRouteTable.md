---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106353"
---
# <span data-ttu-id="26513-101">Get-AzureEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="26513-101">Get-AzureEffectiveRouteTable</span></span>

## <span data-ttu-id="26513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26513-102">SYNOPSIS</span></span>
<span data-ttu-id="26513-103">Bir sanal makinede uygulanan rotayı alır.</span><span class="sxs-lookup"><span data-stu-id="26513-103">Gets the route applied in a virtual machine.</span></span>

## <span data-ttu-id="26513-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26513-104">SYNTAX</span></span>

### <span data-ttu-id="26513-105">IaaSGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="26513-105">IaaSGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="26513-106">SlotGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="26513-106">SlotGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="26513-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="26513-107">DESCRIPTION</span></span>
<span data-ttu-id="26513-108">**Get-AzureEffectiveRouteTable** cmdlet 'i, bir sanal makinede uygulanan rotayı alır.</span><span class="sxs-lookup"><span data-stu-id="26513-108">The **Get-AzureEffectiveRouteTable** cmdlet gets the route applied in a virtual machine.</span></span>
<span data-ttu-id="26513-109">Bu işlemin tamamlanması birkaç saniye sürebilir.</span><span class="sxs-lookup"><span data-stu-id="26513-109">This operation could take several seconds to finish.</span></span>

## <span data-ttu-id="26513-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26513-110">EXAMPLES</span></span>

### <span data-ttu-id="26513-111">Örnek 1: sanal makineyi uygulama</span><span class="sxs-lookup"><span data-stu-id="26513-111">Example 1: Get the effective route applied a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

<span data-ttu-id="26513-112">Bu komut, ContosoService adındaki hizmet için ContosoVM06 adındaki bir sanal makineyi alır ve bu sanal makine nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="26513-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="26513-113">Geçerli cmdlet, bu sanal makineye uygulanan rotayı alır.</span><span class="sxs-lookup"><span data-stu-id="26513-113">The current cmdlet gets the route applied to that virtual machine.</span></span>

## <span data-ttu-id="26513-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26513-114">PARAMETERS</span></span>

### <span data-ttu-id="26513-115">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="26513-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="26513-116">Bu cmdlet 'in etkin yollar aldığı ağ bağdaştırıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26513-116">Specifies the name of the network adapter for which this cmdlet gets effective routes.</span></span>

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

### <span data-ttu-id="26513-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="26513-117">-Profile</span></span>
<span data-ttu-id="26513-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="26513-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="26513-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="26513-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26513-120">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="26513-120">-RoleInstanceName</span></span>
<span data-ttu-id="26513-121">Bu cmdlet 'in etkin yolları aldığı PaaS rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26513-121">Specifies the name of a PaaS role for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26513-122">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="26513-122">-ServiceName</span></span>
<span data-ttu-id="26513-123">Bulut hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26513-123">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="26513-124">Bu cmdlet 'in geçerli yollarla kullandığı PaaS rolü, bu parametrenin belirttiği hizmete aittir.</span><span class="sxs-lookup"><span data-stu-id="26513-124">The PaaS role for which this cmdlet gets effective routes belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="26513-125">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="26513-125">-Slot</span></span>
<span data-ttu-id="26513-126">PaaS yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26513-126">Specifies a PaaS slot.</span></span>
<span data-ttu-id="26513-127">Bu cmdlet 'in geçerli yolların aldığı PaaS rolünde bu parametrenin belirttiği yuva vardır.</span><span class="sxs-lookup"><span data-stu-id="26513-127">The PaaS role for which this cmdlet gets effective routes has the slot that this parameter specifies.</span></span>
<span data-ttu-id="26513-128">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="26513-128">Valid values are:</span></span> 

- <span data-ttu-id="26513-129">Üretim</span><span class="sxs-lookup"><span data-stu-id="26513-129">Production</span></span>
- <span data-ttu-id="26513-130">Geçici saklama</span><span class="sxs-lookup"><span data-stu-id="26513-130">Staging</span></span> 

<span data-ttu-id="26513-131">Varsayılan değer Production değeridir.</span><span class="sxs-lookup"><span data-stu-id="26513-131">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26513-132">-VM</span><span class="sxs-lookup"><span data-stu-id="26513-132">-VM</span></span>
<span data-ttu-id="26513-133">Bu cmdlet 'in geçerli yolları aldığı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="26513-133">Specifies the virtual machine object for which this cmdlet gets effective routes.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26513-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26513-134">CommonParameters</span></span>
<span data-ttu-id="26513-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26513-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26513-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26513-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26513-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26513-137">INPUTS</span></span>

## <span data-ttu-id="26513-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26513-138">OUTPUTS</span></span>

### <span data-ttu-id="26513-139">System. topluluklar. Generic. IEnumerable<Microsoft. Windowsazme. Management. Network. modeller. EffectiveRouteTable, Microsoft. Windowsazme. Management. Network></span><span class="sxs-lookup"><span data-stu-id="26513-139">System.Collections.Generic.IEnumerable<Microsoft.WindowsAzure.Management.Network.Models.EffectiveRouteTable, Microsoft.WindowsAzure.Management.Network></span></span>

## <span data-ttu-id="26513-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26513-140">NOTES</span></span>

## <span data-ttu-id="26513-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26513-141">RELATED LINKS</span></span>

[<span data-ttu-id="26513-142">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="26513-142">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="26513-143">Yeni-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="26513-143">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="26513-144">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="26513-144">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)

[<span data-ttu-id="26513-145">Remove-Azuyeniden yönlendirme</span><span class="sxs-lookup"><span data-stu-id="26513-145">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="26513-146">Set-Azuyeniden gönderiliyor Netroutetable</span><span class="sxs-lookup"><span data-stu-id="26513-146">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


