---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: f074d61919098d6c23ab39424774d9ba18e457d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587614"
---
# <span data-ttu-id="feb38-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="feb38-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="feb38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feb38-102">SYNOPSIS</span></span>
<span data-ttu-id="feb38-103">Bir sanal makineden SQL Server uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="feb38-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="feb38-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="feb38-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="feb38-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="feb38-105">DESCRIPTION</span></span>
<span data-ttu-id="feb38-106">**Remove-AzureRmVMSqlServerExtension** cmdlet 'i, bir AzureSQL sunucu uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="feb38-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="feb38-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="feb38-107">EXAMPLES</span></span>

### <span data-ttu-id="feb38-108">Örnek 1: SQL Server uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="feb38-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="feb38-109">Bu komut, ContosoVM22 adındaki sanal makineden SQL Server uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="feb38-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="feb38-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="feb38-110">PARAMETERS</span></span>

### <span data-ttu-id="feb38-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="feb38-111">-Name</span></span>
<span data-ttu-id="feb38-112">Bu cmdlet 'in kaldırdığı uzantının SQL Server adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="feb38-112">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb38-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb38-113">-ResourceGroupName</span></span>
<span data-ttu-id="feb38-114">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="feb38-114">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb38-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="feb38-115">-VMName</span></span>
<span data-ttu-id="feb38-116">Bu cmdlet 'in SQL Server uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="feb38-116">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb38-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb38-117">CommonParameters</span></span>
<span data-ttu-id="feb38-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="feb38-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb38-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feb38-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb38-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="feb38-120">INPUTS</span></span>

### <span data-ttu-id="feb38-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="feb38-121">None</span></span>
<span data-ttu-id="feb38-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="feb38-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="feb38-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="feb38-123">OUTPUTS</span></span>

## <span data-ttu-id="feb38-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="feb38-124">NOTES</span></span>

## <span data-ttu-id="feb38-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="feb38-125">RELATED LINKS</span></span>

[<span data-ttu-id="feb38-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="feb38-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="feb38-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="feb38-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


