---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E3E0237-8E2D-4B3A-AD0C-2121DDE1AAB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28259b97f382092f5e6293048c040688011cfe92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106152"
---
# <span data-ttu-id="93b67-101">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="93b67-101">Remove-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="93b67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93b67-102">SYNOPSIS</span></span>
<span data-ttu-id="93b67-103">Ağ güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93b67-103">Removes a network security group.</span></span>

## <span data-ttu-id="93b67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93b67-104">SYNTAX</span></span>

### <span data-ttu-id="93b67-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span><span class="sxs-lookup"><span data-stu-id="93b67-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="93b67-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span><span class="sxs-lookup"><span data-stu-id="93b67-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="93b67-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span><span class="sxs-lookup"><span data-stu-id="93b67-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> [-Slot <String>] -RoleName <String>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="93b67-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="93b67-108">DESCRIPTION</span></span>
<span data-ttu-id="93b67-109">**Remove-Azurenetworksecuritation** cmdlet 'i, bir ağ güvenlik grubunu sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93b67-109">The **Remove-AzureNetworkSecurityGroupAssociation** cmdlet removes a network security group from a virtual machine.</span></span>

## <span data-ttu-id="93b67-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93b67-110">EXAMPLES</span></span>

### <span data-ttu-id="93b67-111">Örnek 1: ağ güvenlik grubuna sanal makine kaldırma</span><span class="sxs-lookup"><span data-stu-id="93b67-111">Example 1: Remove a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Remove-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="93b67-112">Bu komut, ContosoService adındaki hizmet için ContosoVM06 adındaki bir sanal makineyi alır ve bu sanal makine nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="93b67-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="93b67-113">Geçerli cmdlet, ContosoNetworkSecurityGroup adlı ağ güvenlik grubunu bu sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93b67-113">The current cmdlet removes the network security group named ContosoNetworkSecurityGroup from that virtual machine.</span></span>

## <span data-ttu-id="93b67-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93b67-114">PARAMETERS</span></span>

### <span data-ttu-id="93b67-115">-Force</span><span class="sxs-lookup"><span data-stu-id="93b67-115">-Force</span></span>
<span data-ttu-id="93b67-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="93b67-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93b67-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="93b67-117">-Name</span></span>
<span data-ttu-id="93b67-118">Bu cmdlet 'in kaldırdığı ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93b67-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="93b67-119">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="93b67-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="93b67-120">Bu cmdlet 'in ağ güvenlik grubunu kaldırdığı ağ bağdaştırıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93b67-120">Specifies the name of the network adapter from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b67-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="93b67-121">-PassThru</span></span>
<span data-ttu-id="93b67-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="93b67-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="93b67-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="93b67-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="93b67-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="93b67-124">-Profile</span></span>
<span data-ttu-id="93b67-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93b67-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93b67-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="93b67-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93b67-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="93b67-127">-RoleName</span></span>
<span data-ttu-id="93b67-128">Bu cmdlet 'in ağ güvenlik grubunu kaldırdığı PaaS rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93b67-128">Specifies the name of a PaaS role from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b67-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="93b67-129">-ServiceName</span></span>
<span data-ttu-id="93b67-130">Bulut hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93b67-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="93b67-131">Bu cmdlet 'in kaldırıldığı PaaS rolü, bu parametrenin belirttiği hizmete aittir.</span><span class="sxs-lookup"><span data-stu-id="93b67-131">The PaaS role from which this cmdlet removes a network security group belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b67-132">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="93b67-132">-Slot</span></span>
<span data-ttu-id="93b67-133">PaaS yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93b67-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="93b67-134">Bu cmdlet 'in kaldırıldığı PaaS rolü, bu parametrenin belirttiği yuvaya sahiptir.</span><span class="sxs-lookup"><span data-stu-id="93b67-134">The PaaS role from which this cmdlet removes a network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="93b67-135">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="93b67-135">Valid values are:</span></span>

- <span data-ttu-id="93b67-136">Üretim</span><span class="sxs-lookup"><span data-stu-id="93b67-136">Production</span></span>
- <span data-ttu-id="93b67-137">Geçici saklama</span><span class="sxs-lookup"><span data-stu-id="93b67-137">Staging</span></span>

<span data-ttu-id="93b67-138">Varsayılan değer Production değeridir.</span><span class="sxs-lookup"><span data-stu-id="93b67-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b67-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="93b67-139">-SubnetName</span></span>
<span data-ttu-id="93b67-140">Bu cmdlet 'in ağ güvenlik grubunu kaldırdığı bir alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93b67-140">Specifies the name of a subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b67-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="93b67-141">-VirtualNetworkName</span></span>
<span data-ttu-id="93b67-142">Bu cmdlet 'in ağ güvenlik grubunu kaldırdığı alt ağı içeren sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93b67-142">Specifies the name of a virtual network that contains the subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b67-143">-VM</span><span class="sxs-lookup"><span data-stu-id="93b67-143">-VM</span></span>
<span data-ttu-id="93b67-144">Bu cmdlet 'in ağ güvenlik grubunu uyguladığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="93b67-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93b67-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b67-145">CommonParameters</span></span>
<span data-ttu-id="93b67-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93b67-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b67-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b67-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b67-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93b67-148">INPUTS</span></span>

## <span data-ttu-id="93b67-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93b67-149">OUTPUTS</span></span>

### <span data-ttu-id="93b67-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93b67-150">System.Boolean</span></span>

## <span data-ttu-id="93b67-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93b67-151">NOTES</span></span>

## <span data-ttu-id="93b67-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93b67-152">RELATED LINKS</span></span>

[<span data-ttu-id="93b67-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="93b67-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="93b67-154">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="93b67-154">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)
