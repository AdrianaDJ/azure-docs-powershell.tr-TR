---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: aa37745469ad6610fa2511d49c3404bbf54d8059
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939770"
---
# <span data-ttu-id="d049d-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d049d-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="d049d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d049d-102">SYNOPSIS</span></span>
<span data-ttu-id="d049d-103">Bir sanal makineden SQL Server uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d049d-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d049d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d049d-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d049d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d049d-105">DESCRIPTION</span></span>
<span data-ttu-id="d049d-106">**Remove-AzureRmVMSqlServerExtension** cmdlet 'i, bir AzureSQL sunucu uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d049d-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="d049d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d049d-107">EXAMPLES</span></span>

### <span data-ttu-id="d049d-108">Örnek 1: SQL Server uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d049d-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="d049d-109">Bu komut, ContosoVM22 adındaki sanal makineden SQL Server uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d049d-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="d049d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d049d-110">PARAMETERS</span></span>

### <span data-ttu-id="d049d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d049d-111">-DefaultProfile</span></span>
<span data-ttu-id="d049d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d049d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d049d-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d049d-113">-Name</span></span>
<span data-ttu-id="d049d-114">Bu cmdlet 'in kaldırdığı uzantının SQL Server adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d049d-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d049d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d049d-115">-ResourceGroupName</span></span>
<span data-ttu-id="d049d-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d049d-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d049d-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="d049d-117">-VMName</span></span>
<span data-ttu-id="d049d-118">Bu cmdlet 'in SQL Server uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d049d-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="d049d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d049d-119">CommonParameters</span></span>
<span data-ttu-id="d049d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d049d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d049d-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d049d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d049d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d049d-122">INPUTS</span></span>

### <span data-ttu-id="d049d-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d049d-123">None</span></span>
<span data-ttu-id="d049d-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d049d-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d049d-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d049d-125">OUTPUTS</span></span>

### <span data-ttu-id="d049d-126">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d049d-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d049d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d049d-127">NOTES</span></span>

## <span data-ttu-id="d049d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d049d-128">RELATED LINKS</span></span>

[<span data-ttu-id="d049d-129">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d049d-129">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="d049d-130">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d049d-130">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


