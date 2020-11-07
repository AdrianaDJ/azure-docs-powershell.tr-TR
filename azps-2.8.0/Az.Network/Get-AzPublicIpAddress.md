---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 38eff375baa948098ac66c8e2b3c3fe1849f3bc0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918452"
---
# <span data-ttu-id="ad1e5-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ad1e5-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="ad1e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad1e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1e5-103">Genel bir IP adresi alır.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-103">Gets a public IP address.</span></span>

## <span data-ttu-id="ad1e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad1e5-104">SYNTAX</span></span>

### <span data-ttu-id="ad1e5-105">NoExpandStandAloneIp (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ad1e5-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad1e5-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="ad1e5-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad1e5-107">Noexpandscalesetıp</span><span class="sxs-lookup"><span data-stu-id="ad1e5-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad1e5-108">Expandscalesetıp</span><span class="sxs-lookup"><span data-stu-id="ad1e5-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad1e5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad1e5-109">DESCRIPTION</span></span>
<span data-ttu-id="ad1e5-110">**Get-Azpublicıpaddress** cmdlet 'i kaynak grubunda bir veya birden çok ortak IP adresi alır.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="ad1e5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad1e5-111">EXAMPLES</span></span>

### <span data-ttu-id="ad1e5-112">1: genel IP kaynağı edinme</span><span class="sxs-lookup"><span data-stu-id="ad1e5-112">1: Get a public IP resource</span></span>
```
Get-AzPublicIpAddress -Name myPublicIp1 -ResourceGroupName myRg

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="ad1e5-113">Bu komut, kaynak grubunda myPublicIp adında Mypublicıp adlı ortak bir IP adresi kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="ad1e5-114">2: filtreleme kullanarak genel IP kaynaklarını alma</span><span class="sxs-lookup"><span data-stu-id="ad1e5-114">2: Get public IP resources using filtering</span></span>
```
Get-AzPublicIpAddress -Name myPublicIp*

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="ad1e5-115">Bu komut, adı myPublicIp ile başlayan tüm genel IP adresi kaynaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="ad1e5-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad1e5-116">PARAMETERS</span></span>

### <span data-ttu-id="ad1e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad1e5-117">-DefaultProfile</span></span>
<span data-ttu-id="ad1e5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1e5-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ad1e5-119">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1e5-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ad1e5-120">-IpConfigurationName</span></span>
<span data-ttu-id="ad1e5-121">Ağ arabirimi IP yapılandırması adı.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-121">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1e5-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad1e5-122">-Name</span></span>
<span data-ttu-id="ad1e5-123">Bu cmdlet 'in aldığı genel IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ad1e5-124">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="ad1e5-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="ad1e5-125">Sanal makine ağı arabirim adı.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-125">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad1e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad1e5-127">Bu cmdlet 'in aldığı ortak IP adresini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ad1e5-128">-Virtualmachineındex</span><span class="sxs-lookup"><span data-stu-id="ad1e5-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="ad1e5-129">Sanal makine dizini.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-129">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1e5-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ad1e5-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="ad1e5-131">Sanal makine ölçek kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-131">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1e5-132">CommonParameters</span></span>
<span data-ttu-id="ad1e5-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1e5-134">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ad1e5-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1e5-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad1e5-135">INPUTS</span></span>

### <span data-ttu-id="ad1e5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ad1e5-136">System.String</span></span>

## <span data-ttu-id="ad1e5-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad1e5-137">OUTPUTS</span></span>

### <span data-ttu-id="ad1e5-138">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="ad1e5-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="ad1e5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad1e5-139">NOTES</span></span>

## <span data-ttu-id="ad1e5-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad1e5-140">RELATED LINKS</span></span>

[<span data-ttu-id="ad1e5-141">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="ad1e5-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="ad1e5-142">Remove-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="ad1e5-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="ad1e5-143">Set-Azpublicıpadresi</span><span class="sxs-lookup"><span data-stu-id="ad1e5-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


