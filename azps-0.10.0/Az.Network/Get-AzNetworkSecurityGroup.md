---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: beb2b723a0b72f7ab485846f6f55fabd4e6ef9aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935523"
---
# <span data-ttu-id="98243-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="98243-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="98243-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98243-102">SYNOPSIS</span></span>
<span data-ttu-id="98243-103">Bir ağ güvenlik grubu alır.</span><span class="sxs-lookup"><span data-stu-id="98243-103">Gets a network security group.</span></span>

## <span data-ttu-id="98243-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98243-104">SYNTAX</span></span>

### <span data-ttu-id="98243-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="98243-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98243-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="98243-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98243-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="98243-107">DESCRIPTION</span></span>
<span data-ttu-id="98243-108">**Get-AzNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="98243-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="98243-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98243-109">EXAMPLES</span></span>

### <span data-ttu-id="98243-110">1: var olan bir ağ güvenlik grubunu alma</span><span class="sxs-lookup"><span data-stu-id="98243-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="98243-111">Bu komut, "RG1" kaynak grubundaki "nsg1" Azure ağ güvenlik grubunun içeriğini döndürüyor</span><span class="sxs-lookup"><span data-stu-id="98243-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="98243-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98243-112">PARAMETERS</span></span>

### <span data-ttu-id="98243-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98243-113">-DefaultProfile</span></span>
<span data-ttu-id="98243-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98243-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98243-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="98243-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98243-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="98243-116">-Name</span></span>
<span data-ttu-id="98243-117">Bu cmdlet 'in aldığı ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98243-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98243-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98243-118">-ResourceGroupName</span></span>
<span data-ttu-id="98243-119">Ağ güvenlik grubunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98243-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98243-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98243-120">CommonParameters</span></span>
<span data-ttu-id="98243-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98243-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98243-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98243-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98243-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98243-123">INPUTS</span></span>

## <span data-ttu-id="98243-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98243-124">OUTPUTS</span></span>

### <span data-ttu-id="98243-125">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="98243-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="98243-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98243-126">NOTES</span></span>

## <span data-ttu-id="98243-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98243-127">RELATED LINKS</span></span>

[<span data-ttu-id="98243-128">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="98243-128">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="98243-129">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="98243-129">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="98243-130">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="98243-130">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


