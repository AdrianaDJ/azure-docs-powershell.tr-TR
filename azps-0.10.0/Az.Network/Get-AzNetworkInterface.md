---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: df769ff4a6e4eb47bc47b881ac8c06de1fdb9e4c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935525"
---
# <span data-ttu-id="d2429-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d2429-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="d2429-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2429-102">SYNOPSIS</span></span>
<span data-ttu-id="d2429-103">Ağ arabirimini alır.</span><span class="sxs-lookup"><span data-stu-id="d2429-103">Gets a network interface.</span></span>

## <span data-ttu-id="d2429-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2429-104">SYNTAX</span></span>

### <span data-ttu-id="d2429-105">NoExpandStandAloneNic (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2429-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2429-106">Expandstandlı</span><span class="sxs-lookup"><span data-stu-id="d2429-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2429-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="d2429-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2429-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="d2429-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2429-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2429-109">DESCRIPTION</span></span>
<span data-ttu-id="d2429-110">**Get-Aznetworkınterface** cmdlet 'ı bir Azure ağ arabirimini veya bir kaynak grubundaki Azure ağ arabirimlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d2429-110">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="d2429-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2429-111">EXAMPLES</span></span>

### <span data-ttu-id="d2429-112">Örnek 1: tüm ağ arabirimlerini alma</span><span class="sxs-lookup"><span data-stu-id="d2429-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzNetworkInterface
```

<span data-ttu-id="d2429-113">Bu komut geçerli aboneliğin tüm ağ arabirimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d2429-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="d2429-114">Örnek 2: belirli bir sağlama durumuyla tüm ağ arabirimlerini alma</span><span class="sxs-lookup"><span data-stu-id="d2429-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="d2429-115">Bu komut, kaynak grubundaki, kaynak grubundaki, sağlama durumu başarılı olan tüm ağ arabirimlerini ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="d2429-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="d2429-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2429-116">PARAMETERS</span></span>

### <span data-ttu-id="d2429-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2429-117">-DefaultProfile</span></span>
<span data-ttu-id="d2429-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2429-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2429-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d2429-119">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2429-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2429-120">-Name</span></span>
<span data-ttu-id="d2429-121">Bu cmdlet 'in aldığı ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2429-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2429-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2429-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2429-123">Bu cmdlet 'in ağ arabirimlerini aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2429-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2429-124">-Virtualmachineındex</span><span class="sxs-lookup"><span data-stu-id="d2429-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="d2429-125">Bu cmdlet 'in ağ arabirimlerini aldığı sanal makine ölçek kümesinin sanal makine dizinini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2429-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2429-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d2429-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="d2429-127">Bu cmdlet 'in ağ arabirimlerini aldığı sanal makine ölçeği kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2429-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2429-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2429-128">CommonParameters</span></span>
<span data-ttu-id="d2429-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2429-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2429-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2429-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2429-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2429-131">INPUTS</span></span>

## <span data-ttu-id="d2429-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2429-132">OUTPUTS</span></span>

### <span data-ttu-id="d2429-133">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d2429-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d2429-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2429-134">NOTES</span></span>

## <span data-ttu-id="d2429-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2429-135">RELATED LINKS</span></span>

[<span data-ttu-id="d2429-136">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d2429-136">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="d2429-137">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d2429-137">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="d2429-138">Set-Azağinterface</span><span class="sxs-lookup"><span data-stu-id="d2429-138">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


