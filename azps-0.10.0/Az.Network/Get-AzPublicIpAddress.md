---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: b9eaacb9a9d779814fc5f0b873aa8e98afedd362
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935488"
---
# <span data-ttu-id="771d2-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="771d2-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="771d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="771d2-102">SYNOPSIS</span></span>
<span data-ttu-id="771d2-103">Genel bir IP adresi alır.</span><span class="sxs-lookup"><span data-stu-id="771d2-103">Gets a public IP address.</span></span>

## <span data-ttu-id="771d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="771d2-104">SYNTAX</span></span>

### <span data-ttu-id="771d2-105">NoExpandStandAloneIp (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="771d2-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="771d2-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="771d2-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="771d2-107">Noexpandscalesetıp</span><span class="sxs-lookup"><span data-stu-id="771d2-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="771d2-108">Expandscalesetıp</span><span class="sxs-lookup"><span data-stu-id="771d2-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="771d2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="771d2-109">DESCRIPTION</span></span>
<span data-ttu-id="771d2-110">**Get-Azpublicıpaddress** cmdlet 'i kaynak grubunda bir veya birden çok ortak IP adresi alır.</span><span class="sxs-lookup"><span data-stu-id="771d2-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="771d2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="771d2-111">EXAMPLES</span></span>

### <span data-ttu-id="771d2-112">1: genel IP kaynağı edinme</span><span class="sxs-lookup"><span data-stu-id="771d2-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="771d2-113">Bu komut, kaynak grubunda $rgName adı $publicIPName olan ortak bir IP adresi kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="771d2-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="771d2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="771d2-114">PARAMETERS</span></span>

### <span data-ttu-id="771d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="771d2-115">-DefaultProfile</span></span>
<span data-ttu-id="771d2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="771d2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="771d2-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="771d2-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771d2-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="771d2-118">-IpConfigurationName</span></span>
<span data-ttu-id="771d2-119">Ağ arabirimi IP yapılandırması adı.</span><span class="sxs-lookup"><span data-stu-id="771d2-119">Network Interface IP Configuration Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771d2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="771d2-120">-Name</span></span>
<span data-ttu-id="771d2-121">Bu cmdlet 'in aldığı genel IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="771d2-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771d2-122">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="771d2-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="771d2-123">Sanal makine ağı arabirim adı.</span><span class="sxs-lookup"><span data-stu-id="771d2-123">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="771d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="771d2-125">Bu cmdlet 'in aldığı ortak IP adresini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="771d2-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771d2-126">-Virtualmachineındex</span><span class="sxs-lookup"><span data-stu-id="771d2-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="771d2-127">Sanal makine dizini.</span><span class="sxs-lookup"><span data-stu-id="771d2-127">Virtual Machine Index.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771d2-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="771d2-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="771d2-129">Sanal makine ölçek kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="771d2-129">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="771d2-130">CommonParameters</span></span>
<span data-ttu-id="771d2-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="771d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="771d2-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="771d2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="771d2-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="771d2-133">INPUTS</span></span>

## <span data-ttu-id="771d2-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="771d2-134">OUTPUTS</span></span>

### <span data-ttu-id="771d2-135">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="771d2-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="771d2-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="771d2-136">NOTES</span></span>

## <span data-ttu-id="771d2-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="771d2-137">RELATED LINKS</span></span>

[<span data-ttu-id="771d2-138">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="771d2-138">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="771d2-139">Remove-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="771d2-139">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="771d2-140">Set-Azpublicıpadresi</span><span class="sxs-lookup"><span data-stu-id="771d2-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


