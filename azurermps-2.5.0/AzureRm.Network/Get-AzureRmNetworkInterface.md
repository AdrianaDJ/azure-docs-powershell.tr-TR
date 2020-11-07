---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 263293ea117f85caf32029ee0cfbf0dff2142cc3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940079"
---
# <span data-ttu-id="75196-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="75196-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="75196-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75196-102">SYNOPSIS</span></span>
<span data-ttu-id="75196-103">Ağ arabirimini alır.</span><span class="sxs-lookup"><span data-stu-id="75196-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75196-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75196-104">SYNTAX</span></span>

### <span data-ttu-id="75196-105">NoExpandStandAloneNic (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="75196-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75196-106">Expandstandlı</span><span class="sxs-lookup"><span data-stu-id="75196-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75196-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="75196-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75196-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="75196-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75196-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="75196-109">DESCRIPTION</span></span>
<span data-ttu-id="75196-110">**Get-Azurermnetworkınterface** cmdlet 'ı bir Azure ağ arabirimini veya kaynak grubundaki Azure ağ arabirimlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="75196-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="75196-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75196-111">EXAMPLES</span></span>

### <span data-ttu-id="75196-112">Örnek 1: tüm ağ arabirimlerini alma</span><span class="sxs-lookup"><span data-stu-id="75196-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="75196-113">Bu komut geçerli aboneliğin tüm ağ arabirimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="75196-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="75196-114">Örnek 2: belirli bir sağlama durumuyla tüm ağ arabirimlerini alma</span><span class="sxs-lookup"><span data-stu-id="75196-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="75196-115">Bu komut, kaynak grubundaki, kaynak grubundaki, sağlama durumu başarılı olan tüm ağ arabirimlerini ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="75196-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="75196-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75196-116">PARAMETERS</span></span>

### <span data-ttu-id="75196-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75196-117">-DefaultProfile</span></span>
<span data-ttu-id="75196-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75196-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75196-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="75196-119">-ExpandResource</span></span>
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

### <span data-ttu-id="75196-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="75196-120">-Name</span></span>
<span data-ttu-id="75196-121">Bu cmdlet 'in aldığı ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75196-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

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

### <span data-ttu-id="75196-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75196-122">-ResourceGroupName</span></span>
<span data-ttu-id="75196-123">Bu cmdlet 'in ağ arabirimlerini aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75196-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="75196-124">-Virtualmachineındex</span><span class="sxs-lookup"><span data-stu-id="75196-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="75196-125">Bu cmdlet 'in ağ arabirimlerini aldığı sanal makine ölçek kümesinin sanal makine dizinini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75196-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="75196-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="75196-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="75196-127">Bu cmdlet 'in ağ arabirimlerini aldığı sanal makine ölçeği kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75196-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="75196-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75196-128">CommonParameters</span></span>
<span data-ttu-id="75196-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75196-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75196-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75196-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75196-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75196-131">INPUTS</span></span>

## <span data-ttu-id="75196-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75196-132">OUTPUTS</span></span>

### <span data-ttu-id="75196-133">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="75196-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="75196-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75196-134">NOTES</span></span>

## <span data-ttu-id="75196-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75196-135">RELATED LINKS</span></span>

[<span data-ttu-id="75196-136">Yeni-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="75196-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="75196-137">Remove-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="75196-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="75196-138">Set-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="75196-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


