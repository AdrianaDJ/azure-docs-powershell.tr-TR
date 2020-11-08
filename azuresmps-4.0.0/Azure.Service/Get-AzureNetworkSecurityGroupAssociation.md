---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106582"
---
# <span data-ttu-id="3f7b9-101">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="3f7b9-101">Get-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="3f7b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f7b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3f7b9-103">Sanal makine, ağ bağdaştırıcısı veya PaaS rolü için bir ağ güvenliği grubu alır.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-103">Gets a network security group for a virtual machine, network adapter, or PaaS role.</span></span>

## <span data-ttu-id="3f7b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f7b9-104">SYNTAX</span></span>

### <span data-ttu-id="3f7b9-105">GetNetworkSecurityGroupAssociationForSubnet</span><span class="sxs-lookup"><span data-stu-id="3f7b9-105">GetNetworkSecurityGroupAssociationForSubnet</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3f7b9-106">GetNetworkSecurityGroupAssociationForIaaSRole</span><span class="sxs-lookup"><span data-stu-id="3f7b9-106">GetNetworkSecurityGroupAssociationForIaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3f7b9-107">GetNetworkSecurityGroupAssociationForPaaSRole</span><span class="sxs-lookup"><span data-stu-id="3f7b9-107">GetNetworkSecurityGroupAssociationForPaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f7b9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f7b9-108">DESCRIPTION</span></span>
<span data-ttu-id="3f7b9-109">**Get-Azurenetworksecuritation** cmdlet 'i bir sanal makine, ağ bağdaştırıcısı veya platformun hizmet (PaaS) rolü olarak ağ güvenliği grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-109">The **Get-AzureNetworkSecurityGroupAssociation** cmdlet gets the network security group for a virtual machine, network adapter, or platform as a service (PaaS) role.</span></span>

## <span data-ttu-id="3f7b9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f7b9-110">EXAMPLES</span></span>

### <span data-ttu-id="3f7b9-111">Örnek 1: sanal makinenin ağ güvenlik grubunu alma</span><span class="sxs-lookup"><span data-stu-id="3f7b9-111">Example 1: Get the network security group for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

<span data-ttu-id="3f7b9-112">Bu komut, ContosoService adındaki hizmet için ContosoVM06 adındaki bir sanal makineyi alır ve bu sanal makine nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="3f7b9-113">Geçerli cmdlet, bu sanal makineyle ilişkilendirilmiş ağ güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-113">The current cmdlet gets the network security group associated to that virtual machine.</span></span>

## <span data-ttu-id="3f7b9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f7b9-114">PARAMETERS</span></span>

### <span data-ttu-id="3f7b9-115">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="3f7b9-115">-Detailed</span></span>
<span data-ttu-id="3f7b9-116">Bu cmdlet 'in sanal makineyle ilişkili ağ güvenlik grubunun ayrıntılarını döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-116">Indicates that this cmdlet returns details of the network security group that is associated to the virtual machine.</span></span>
<span data-ttu-id="3f7b9-117">Bu ayrıntılar konum ve kuralları içerir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-117">These details include location and rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7b9-118">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="3f7b9-118">-NetworkInterfaceName</span></span>
<span data-ttu-id="3f7b9-119">Bu cmdlet 'in ağ güvenlik grubunu aldığı ağ bağdaştırıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-119">Specifies the name of the network adapter for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7b9-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f7b9-120">-Profile</span></span>
<span data-ttu-id="3f7b9-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3f7b9-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f7b9-123">-RoleName</span><span class="sxs-lookup"><span data-stu-id="3f7b9-123">-RoleName</span></span>
<span data-ttu-id="3f7b9-124">Bu cmdlet 'in ağ güvenlik grubunu aldığı PaaS rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-124">Specifies the name of a PaaS role for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7b9-125">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="3f7b9-125">-ServiceName</span></span>
<span data-ttu-id="3f7b9-126">Bulut hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-126">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="3f7b9-127">PaaS rolü, bu parametrenin belirttiği hizmete aittir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-127">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7b9-128">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="3f7b9-128">-Slot</span></span>
<span data-ttu-id="3f7b9-129">PaaS yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-129">Specifies a PaaS slot.</span></span>
<span data-ttu-id="3f7b9-130">Bu cmdlet 'in aldığı PaaS rolünde bu parametrenin belirttiği yuva vardır.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-130">The PaaS role for which this cmdlet gets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="3f7b9-131">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="3f7b9-131">Valid values are:</span></span> 

- <span data-ttu-id="3f7b9-132">Üretim</span><span class="sxs-lookup"><span data-stu-id="3f7b9-132">Production</span></span>
- <span data-ttu-id="3f7b9-133">Geçici saklama</span><span class="sxs-lookup"><span data-stu-id="3f7b9-133">Staging</span></span> 

<span data-ttu-id="3f7b9-134">Varsayılan değer Production değeridir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-134">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7b9-135">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3f7b9-135">-SubnetName</span></span>
<span data-ttu-id="3f7b9-136">Bu cmdlet 'in ağ güvenlik grubunu aldığı alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-136">Specifies the name of a subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7b9-137">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3f7b9-137">-VirtualNetworkName</span></span>
<span data-ttu-id="3f7b9-138">Bu cmdlet 'in ağ güvenlik grubunu aldığı alt ağı içeren sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-138">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7b9-139">-VM</span><span class="sxs-lookup"><span data-stu-id="3f7b9-139">-VM</span></span>
<span data-ttu-id="3f7b9-140">Bu cmdlet 'in ağ güvenlik grubunu uyguladığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-140">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7b9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f7b9-141">CommonParameters</span></span>
<span data-ttu-id="3f7b9-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f7b9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f7b9-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f7b9-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f7b9-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f7b9-144">INPUTS</span></span>

## <span data-ttu-id="3f7b9-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f7b9-145">OUTPUTS</span></span>

### <span data-ttu-id="3f7b9-146">Microsoft. Windowsazme. Commands. ServiceManagement. Network. NetworkSecurityGroup. model. ınetworksecuritygroup</span><span class="sxs-lookup"><span data-stu-id="3f7b9-146">Microsoft.WindowsAzure.Commands.ServiceManagement.Network.NetworkSecurityGroup.Model.INetworkSecurityGroup</span></span>

## <span data-ttu-id="3f7b9-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f7b9-147">NOTES</span></span>

## <span data-ttu-id="3f7b9-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f7b9-148">RELATED LINKS</span></span>

[<span data-ttu-id="3f7b9-149">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="3f7b9-149">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="3f7b9-150">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="3f7b9-150">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)


