---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938393"
---
# <span data-ttu-id="5135e-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5135e-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="5135e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5135e-102">SYNOPSIS</span></span>
<span data-ttu-id="5135e-103">VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5135e-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="5135e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5135e-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5135e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5135e-105">DESCRIPTION</span></span>
<span data-ttu-id="5135e-106">VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5135e-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="5135e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5135e-107">EXAMPLES</span></span>

### <span data-ttu-id="5135e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5135e-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="5135e-109">Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5135e-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="5135e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5135e-110">PARAMETERS</span></span>

### <span data-ttu-id="5135e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5135e-111">-DefaultProfile</span></span>
<span data-ttu-id="5135e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5135e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5135e-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="5135e-113">-ExtensionName</span></span>
<span data-ttu-id="5135e-114">Uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="5135e-114">The extension name.</span></span>
<span data-ttu-id="5135e-115">Bu parametre belirtilmezse, kullanılan varsayılan değerler Windows VM 'ler için AzureDiskEncryption ve Linux VM 'Ler için AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="5135e-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5135e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5135e-116">-ResourceGroupName</span></span>
<span data-ttu-id="5135e-117">Sanal makine ölçek kümesinin kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5135e-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5135e-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5135e-118">-VMScaleSetName</span></span>
<span data-ttu-id="5135e-119">Sanal makine ölçek kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="5135e-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5135e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5135e-120">CommonParameters</span></span>
<span data-ttu-id="5135e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5135e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5135e-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5135e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5135e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5135e-123">INPUTS</span></span>

### <span data-ttu-id="5135e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5135e-124">System.String</span></span>

## <span data-ttu-id="5135e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5135e-125">OUTPUTS</span></span>

### <span data-ttu-id="5135e-126">Microsoft. Azure. Commands. COMPUTE. modeller. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="5135e-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="5135e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5135e-127">NOTES</span></span>

## <span data-ttu-id="5135e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5135e-128">RELATED LINKS</span></span>