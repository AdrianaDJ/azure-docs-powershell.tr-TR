---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: b6d71d4c80ba30fc02bb22695132a304f94416cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589507"
---
# <span data-ttu-id="f8678-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8678-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="f8678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8678-102">SYNOPSIS</span></span>
<span data-ttu-id="f8678-103">Genel bir IP adresi alır.</span><span class="sxs-lookup"><span data-stu-id="f8678-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8678-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8678-104">SYNTAX</span></span>

### <span data-ttu-id="f8678-105">NoExpandStandAloneIp (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f8678-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8678-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="f8678-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8678-107">Noexpandscalesetıp</span><span class="sxs-lookup"><span data-stu-id="f8678-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8678-108">Expandscalesetıp</span><span class="sxs-lookup"><span data-stu-id="f8678-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8678-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8678-109">DESCRIPTION</span></span>
<span data-ttu-id="f8678-110">**Get-Azurermpublicıpaddress** cmdlet 'i kaynak grubunda bir veya birden çok ortak IP adresini alır.</span><span class="sxs-lookup"><span data-stu-id="f8678-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="f8678-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8678-111">EXAMPLES</span></span>

### <span data-ttu-id="f8678-112">1: genel IP kaynağı edinme</span><span class="sxs-lookup"><span data-stu-id="f8678-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="f8678-113">Bu komut, kaynak grubunda $rgName adı $publicIPName olan ortak bir IP adresi kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="f8678-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="f8678-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8678-114">PARAMETERS</span></span>

### <span data-ttu-id="f8678-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8678-115">-DefaultProfile</span></span>
<span data-ttu-id="f8678-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8678-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8678-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f8678-117">-ExpandResource</span></span>
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

### <span data-ttu-id="f8678-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f8678-118">-IpConfigurationName</span></span>
<span data-ttu-id="f8678-119">Ağ arabirimi IP yapılandırması adı.</span><span class="sxs-lookup"><span data-stu-id="f8678-119">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="f8678-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8678-120">-Name</span></span>
<span data-ttu-id="f8678-121">Bu cmdlet 'in aldığı genel IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8678-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8678-122">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="f8678-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="f8678-123">Sanal makine ağı arabirim adı.</span><span class="sxs-lookup"><span data-stu-id="f8678-123">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="f8678-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8678-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8678-125">Bu cmdlet 'in aldığı ortak IP adresini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8678-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8678-126">-Virtualmachineındex</span><span class="sxs-lookup"><span data-stu-id="f8678-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="f8678-127">Sanal makine dizini.</span><span class="sxs-lookup"><span data-stu-id="f8678-127">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="f8678-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f8678-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="f8678-129">Sanal makine ölçek kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="f8678-129">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="f8678-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8678-130">CommonParameters</span></span>
<span data-ttu-id="f8678-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8678-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8678-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8678-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8678-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8678-133">INPUTS</span></span>

### <span data-ttu-id="f8678-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f8678-134">System.String</span></span>

## <span data-ttu-id="f8678-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8678-135">OUTPUTS</span></span>

### <span data-ttu-id="f8678-136">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="f8678-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f8678-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8678-137">NOTES</span></span>

## <span data-ttu-id="f8678-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8678-138">RELATED LINKS</span></span>

[<span data-ttu-id="f8678-139">Yeni-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="f8678-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="f8678-140">Remove-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="f8678-140">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="f8678-141">Set-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="f8678-141">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


