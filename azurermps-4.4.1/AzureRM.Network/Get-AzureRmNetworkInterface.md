---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
ms.openlocfilehash: 42d5ef31b49f8abe5c8e582e0a85e8766a71b9a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594232"
---
# <span data-ttu-id="d3b48-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d3b48-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="d3b48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3b48-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b48-103">Ağ arabirimini alır.</span><span class="sxs-lookup"><span data-stu-id="d3b48-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3b48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3b48-104">SYNTAX</span></span>

### <span data-ttu-id="d3b48-105">NoExpandStandAloneNic (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3b48-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3b48-106">Expandstandlı</span><span class="sxs-lookup"><span data-stu-id="d3b48-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3b48-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="d3b48-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3b48-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="d3b48-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3b48-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3b48-109">DESCRIPTION</span></span>
<span data-ttu-id="d3b48-110">**Get-Azurermnetworkınterface** cmdlet 'ı bir Azure ağ arabirimini veya kaynak grubundaki Azure ağ arabirimlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d3b48-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="d3b48-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3b48-111">EXAMPLES</span></span>

### <span data-ttu-id="d3b48-112">Örnek 1: tüm ağ arabirimlerini alma</span><span class="sxs-lookup"><span data-stu-id="d3b48-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="d3b48-113">Bu komut geçerli aboneliğin tüm ağ arabirimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d3b48-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="d3b48-114">Örnek 2: belirli bir sağlama durumuyla tüm ağ arabirimlerini alma</span><span class="sxs-lookup"><span data-stu-id="d3b48-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="d3b48-115">Bu komut, kaynak grubundaki, kaynak grubundaki, sağlama durumu başarılı olan tüm ağ arabirimlerini ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="d3b48-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="d3b48-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3b48-116">PARAMETERS</span></span>

### <span data-ttu-id="d3b48-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d3b48-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b48-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3b48-118">-Name</span></span>
<span data-ttu-id="d3b48-119">Bu cmdlet 'in aldığı ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3b48-119">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b48-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b48-120">-ResourceGroupName</span></span>
<span data-ttu-id="d3b48-121">Bu cmdlet 'in ağ arabirimlerini aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3b48-121">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b48-122">-Virtualmachineındex</span><span class="sxs-lookup"><span data-stu-id="d3b48-122">-VirtualMachineIndex</span></span>
<span data-ttu-id="d3b48-123">Bu cmdlet 'in ağ arabirimlerini aldığı sanal makine ölçek kümesinin sanal makine dizinini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3b48-123">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b48-124">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d3b48-124">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="d3b48-125">Bu cmdlet 'in ağ arabirimlerini aldığı sanal makine ölçeği kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3b48-125">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b48-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b48-126">-DefaultProfile</span></span>
<span data-ttu-id="d3b48-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3b48-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3b48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b48-128">CommonParameters</span></span>
<span data-ttu-id="d3b48-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3b48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b48-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3b48-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b48-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3b48-131">INPUTS</span></span>

## <span data-ttu-id="d3b48-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3b48-132">OUTPUTS</span></span>

### <span data-ttu-id="d3b48-133">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d3b48-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d3b48-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3b48-134">NOTES</span></span>

## <span data-ttu-id="d3b48-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3b48-135">RELATED LINKS</span></span>

[<span data-ttu-id="d3b48-136">Yeni-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d3b48-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="d3b48-137">Remove-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d3b48-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="d3b48-138">Set-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d3b48-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


