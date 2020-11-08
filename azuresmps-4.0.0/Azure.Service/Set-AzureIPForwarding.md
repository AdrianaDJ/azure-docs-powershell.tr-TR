---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105956"
---
# <span data-ttu-id="a2477-101">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="a2477-101">Set-AzureIPForwarding</span></span>

## <span data-ttu-id="a2477-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2477-102">SYNOPSIS</span></span>
<span data-ttu-id="a2477-103">IP iletimini devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a2477-103">Enables or disables IP forwarding.</span></span>

## <span data-ttu-id="a2477-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2477-104">SYNTAX</span></span>

### <span data-ttu-id="a2477-105">Enableıaasipforwardingparamset</span><span class="sxs-lookup"><span data-stu-id="a2477-105">EnableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a2477-106">Disableıaasipforwardingparamset</span><span class="sxs-lookup"><span data-stu-id="a2477-106">DisableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a2477-107">Enableslotıpforwardingparamset</span><span class="sxs-lookup"><span data-stu-id="a2477-107">EnableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a2477-108">Disableslotıpforwardingparamset</span><span class="sxs-lookup"><span data-stu-id="a2477-108">DisableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a2477-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2477-109">DESCRIPTION</span></span>
<span data-ttu-id="a2477-110">**Set-AzureIPForwarding** cmdlet 'i sanal makine, bir platform hizmet (PaaS) rolü veya sanal makineye veya PaaS rolüne ait bir ağ bağdaştırıcısıyla IP iletimini devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a2477-110">The **Set-AzureIPForwarding** cmdlet enables or disables IP forwarding for a virtual machine, for a platform as a service (PaaS) role, or a network adapter that belongs to a virtual machine or PaaS role.</span></span>

## <span data-ttu-id="a2477-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2477-111">EXAMPLES</span></span>

### <span data-ttu-id="a2477-112">Örnek 1: sanal makine için IP iletimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a2477-112">Example 1: Enable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

<span data-ttu-id="a2477-113">Bu komut, ContosoService adındaki hizmet için ContosoVM06 adındaki bir sanal makineyi alır ve bu sanal makine nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="a2477-113">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="a2477-114">Geçerli cmdlet, bu sanal makinenin IP iletimini olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="a2477-114">The current cmdlet enables IP forwarding for that virtual machine.</span></span>

### <span data-ttu-id="a2477-115">Örnek 2: sanal makine için IP iletimini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a2477-115">Example 2: Disable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

<span data-ttu-id="a2477-116">Bu komut, ContosoService adındaki hizmet için ContosoVM06 adındaki bir sanal makineyi alır ve bu sanal makine nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="a2477-116">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="a2477-117">Geçerli cmdlet, bu sanal makinenin IP iletimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a2477-117">The current cmdlet disables IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="a2477-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2477-118">PARAMETERS</span></span>

### <span data-ttu-id="a2477-119">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="a2477-119">-Disable</span></span>
<span data-ttu-id="a2477-120">Bu cmdlet 'in IP iletimini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2477-120">Indicates that this cmdlet disables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2477-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="a2477-121">-Enable</span></span>
<span data-ttu-id="a2477-122">Bu cmdlet 'in IP iletimini etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2477-122">Indicates that this cmdlet enables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2477-123">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="a2477-123">-NetworkInterfaceName</span></span>
<span data-ttu-id="a2477-124">Bu cmdlet 'in IP iletimini ayarladığı ağ bağdaştırıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2477-124">Specifies the name of the network adapter on which this cmdlet sets IP forwarding.</span></span>

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

### <span data-ttu-id="a2477-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a2477-125">-PassThru</span></span>
<span data-ttu-id="a2477-126">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a2477-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a2477-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a2477-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a2477-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="a2477-128">-Profile</span></span>
<span data-ttu-id="a2477-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2477-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2477-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a2477-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2477-131">-RoleName</span><span class="sxs-lookup"><span data-stu-id="a2477-131">-RoleName</span></span>
<span data-ttu-id="a2477-132">Bu cmdlet 'in IP iletimini ayarladığı PaaS rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2477-132">Specifies the name of a PaaS role on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2477-133">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="a2477-133">-ServiceName</span></span>
<span data-ttu-id="a2477-134">Bulut hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2477-134">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="a2477-135">PaaS rolü, bu parametrenin belirttiği hizmete aittir.</span><span class="sxs-lookup"><span data-stu-id="a2477-135">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2477-136">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="a2477-136">-Slot</span></span>
<span data-ttu-id="a2477-137">PaaS yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2477-137">Specifies a PaaS slot.</span></span>
<span data-ttu-id="a2477-138">Bu cmdlet 'in iletimini ayarladığı PaaS rolünde bu parametrenin belirttiği yuva vardır.</span><span class="sxs-lookup"><span data-stu-id="a2477-138">The PaaS role for which this cmdlet sets forwarding has the slot that this parameter specifies.</span></span>
<span data-ttu-id="a2477-139">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a2477-139">Valid values are:</span></span>

- <span data-ttu-id="a2477-140">Üretim</span><span class="sxs-lookup"><span data-stu-id="a2477-140">Production</span></span>
- <span data-ttu-id="a2477-141">Geçici saklama</span><span class="sxs-lookup"><span data-stu-id="a2477-141">Staging</span></span>

<span data-ttu-id="a2477-142">Varsayılan değer Production değeridir.</span><span class="sxs-lookup"><span data-stu-id="a2477-142">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2477-143">-VM</span><span class="sxs-lookup"><span data-stu-id="a2477-143">-VM</span></span>
<span data-ttu-id="a2477-144">Bu cmdlet 'in IP iletimini ayarladığı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2477-144">Specifies the virtual machine object on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2477-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2477-145">CommonParameters</span></span>
<span data-ttu-id="a2477-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2477-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2477-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2477-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2477-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2477-148">INPUTS</span></span>

## <span data-ttu-id="a2477-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2477-149">OUTPUTS</span></span>

### <span data-ttu-id="a2477-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2477-150">System.Boolean</span></span>

## <span data-ttu-id="a2477-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2477-151">NOTES</span></span>

## <span data-ttu-id="a2477-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2477-152">RELATED LINKS</span></span>

[<span data-ttu-id="a2477-153">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="a2477-153">Get-AzureIPForwarding</span></span>](./Get-AzureIPForwarding.md)
