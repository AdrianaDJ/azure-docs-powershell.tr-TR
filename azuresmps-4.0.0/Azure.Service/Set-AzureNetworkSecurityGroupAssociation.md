---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 64639A35-0573-48C8-AB21-19FEB09537BA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b1b251a5fef3ad91f830e18714796421d2abca7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105758"
---
# <span data-ttu-id="f6e38-101">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="f6e38-101">Set-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="f6e38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6e38-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e38-103">Ağ güvenlik grubunu sanal makineyle, PaaS rolüyle veya ağ bağdaştırıcısıyla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-103">Associates a network security group to a virtual machine, PaaS role, or network adapter.</span></span>

## <span data-ttu-id="f6e38-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6e38-104">SYNTAX</span></span>

### <span data-ttu-id="f6e38-105">AddNetworkSecurityGroupAssociationToSubnet</span><span class="sxs-lookup"><span data-stu-id="f6e38-105">AddNetworkSecurityGroupAssociationToSubnet</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VirtualNetworkName <String>
 -SubnetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f6e38-106">AddNetworkSecurityGroupAssociationToIaaSRole</span><span class="sxs-lookup"><span data-stu-id="f6e38-106">AddNetworkSecurityGroupAssociationToIaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VM <PersistentVMRoleContext>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f6e38-107">AddNetworkSecurityGroupAssociationToPaaSRole</span><span class="sxs-lookup"><span data-stu-id="f6e38-107">AddNetworkSecurityGroupAssociationToPaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] [-Slot <String>]
 -RoleName <String> -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6e38-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6e38-108">DESCRIPTION</span></span>
<span data-ttu-id="f6e38-109">**Set-AzureNetworkSecurityGroupAssociation** cmdlet 'i, bir ağ güvenlik grubunu bir sanal makineyle, hizmet (PaaS) rolüyle veya ağ bağdaştırıcısıyla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-109">The **Set-AzureNetworkSecurityGroupAssociation** cmdlet associates a network security group to a virtual machine, platform as a service (PaaS) role, or network adapter.</span></span>

## <span data-ttu-id="f6e38-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6e38-110">EXAMPLES</span></span>

### <span data-ttu-id="f6e38-111">Örnek 1: ağ güvenlik grubuna sanal makine atama</span><span class="sxs-lookup"><span data-stu-id="f6e38-111">Example 1: Assign a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="f6e38-112">Bu komut, ContosoService adındaki hizmet için ContosoVM06 adındaki bir sanal makineyi alır ve bu sanal makine nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="f6e38-113">Geçerli cmdlet, ContosoNetworkSecurityGroup adlı ağ güvenlik grubunu bu sanal makineye atar.</span><span class="sxs-lookup"><span data-stu-id="f6e38-113">The current cmdlet assigns the network security group named ContosoNetworkSecurityGroup to that virtual machine.</span></span>

## <span data-ttu-id="f6e38-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6e38-114">PARAMETERS</span></span>

### <span data-ttu-id="f6e38-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f6e38-115">-Force</span></span>
<span data-ttu-id="f6e38-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f6e38-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f6e38-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6e38-117">-Name</span></span>
<span data-ttu-id="f6e38-118">Bu cmdlet 'in ayarladığı ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-118">Specifies the name of the network security group that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f6e38-119">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="f6e38-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="f6e38-120">Bu cmdlet 'in ağ güvenlik grubunu uyguladığı ağ bağdaştırıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-120">Specifies the name of the network adapter to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e38-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f6e38-121">-PassThru</span></span>
<span data-ttu-id="f6e38-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f6e38-122">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f6e38-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f6e38-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f6e38-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="f6e38-124">-Profile</span></span>
<span data-ttu-id="f6e38-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f6e38-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f6e38-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f6e38-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="f6e38-127">-RoleName</span></span>
<span data-ttu-id="f6e38-128">Bu cmdlet 'in ağ güvenlik grubunu uyguladığı PaaS rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-128">Specifies the name of a PaaS role to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e38-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="f6e38-129">-ServiceName</span></span>
<span data-ttu-id="f6e38-130">Bulut hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="f6e38-131">PaaS rolü, bu parametrenin belirttiği hizmete aittir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-131">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e38-132">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="f6e38-132">-Slot</span></span>
<span data-ttu-id="f6e38-133">PaaS yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="f6e38-134">Bu cmdlet 'in ağ güvenlik grubunda ayarladığı PaaS rolü, bu parametrenin belirttiği yuvaya sahiptir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-134">The PaaS role for which this cmdlet sets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="f6e38-135">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f6e38-135">Valid values are:</span></span> 

- <span data-ttu-id="f6e38-136">Üretim</span><span class="sxs-lookup"><span data-stu-id="f6e38-136">Production</span></span>
- <span data-ttu-id="f6e38-137">Geçici saklama</span><span class="sxs-lookup"><span data-stu-id="f6e38-137">Staging</span></span> 

<span data-ttu-id="f6e38-138">Varsayılan değer Production değeridir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e38-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f6e38-139">-SubnetName</span></span>
<span data-ttu-id="f6e38-140">Bu cmdlet 'in ağ güvenlik grubunu ilişkilendiğinde alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-140">Specifies the name of a subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e38-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f6e38-141">-VirtualNetworkName</span></span>
<span data-ttu-id="f6e38-142">Bu cmdlet 'in ağ güvenlik grubunu ilişkilendiğinde alt ağını içeren sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-142">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e38-143">-VM</span><span class="sxs-lookup"><span data-stu-id="f6e38-143">-VM</span></span>
<span data-ttu-id="f6e38-144">Bu cmdlet 'in ağ güvenlik grubunu uyguladığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6e38-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e38-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e38-145">CommonParameters</span></span>
<span data-ttu-id="f6e38-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6e38-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e38-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6e38-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e38-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6e38-148">INPUTS</span></span>

## <span data-ttu-id="f6e38-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6e38-149">OUTPUTS</span></span>

### <span data-ttu-id="f6e38-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6e38-150">System.Boolean</span></span>

## <span data-ttu-id="f6e38-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6e38-151">NOTES</span></span>

## <span data-ttu-id="f6e38-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6e38-152">RELATED LINKS</span></span>

[<span data-ttu-id="f6e38-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="f6e38-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="f6e38-154">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="f6e38-154">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)


