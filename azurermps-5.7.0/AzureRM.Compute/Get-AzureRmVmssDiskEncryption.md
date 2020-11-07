---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 5aec9973e254f7f30d26b36c64e70903817a5ba7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762655"
---
# <span data-ttu-id="07456-101">Get-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="07456-101">Get-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="07456-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07456-102">SYNOPSIS</span></span>
<span data-ttu-id="07456-103">VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="07456-103">Shows the disk encryption status of a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07456-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07456-104">SYNTAX</span></span>

```
Get-AzureRmVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07456-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07456-105">DESCRIPTION</span></span>
<span data-ttu-id="07456-106">VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="07456-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="07456-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07456-107">EXAMPLES</span></span>

### <span data-ttu-id="07456-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="07456-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="07456-109">Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VM Ölçek kümesinin disk şifreleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="07456-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="07456-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07456-110">PARAMETERS</span></span>

### <span data-ttu-id="07456-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07456-111">-DefaultProfile</span></span>
<span data-ttu-id="07456-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07456-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07456-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="07456-113">-ExtensionName</span></span>
<span data-ttu-id="07456-114">Uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="07456-114">The extension name.</span></span>
<span data-ttu-id="07456-115">Bu parametre belirtilmezse, kullanılan varsayılan değerler Windows VM 'ler için AzureDiskEncryption ve Linux VM 'Ler için AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="07456-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07456-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07456-116">-ResourceGroupName</span></span>
<span data-ttu-id="07456-117">Sanal makine ölçek kümesinin kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="07456-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07456-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="07456-118">-VMScaleSetName</span></span>
<span data-ttu-id="07456-119">Sanal makine ölçek kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="07456-119">The virtual machine scale set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07456-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07456-120">CommonParameters</span></span>
<span data-ttu-id="07456-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07456-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07456-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07456-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07456-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07456-123">INPUTS</span></span>

### <span data-ttu-id="07456-124">System. String</span><span class="sxs-lookup"><span data-stu-id="07456-124">System.String</span></span>

## <span data-ttu-id="07456-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07456-125">OUTPUTS</span></span>

### <span data-ttu-id="07456-126">Microsoft. Azure. Commands. COMPUTE. modeller. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="07456-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="07456-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07456-127">NOTES</span></span>

## <span data-ttu-id="07456-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07456-128">RELATED LINKS</span></span>