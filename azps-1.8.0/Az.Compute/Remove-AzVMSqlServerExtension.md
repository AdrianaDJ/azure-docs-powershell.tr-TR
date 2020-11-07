---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 630df5bbe6677c7019d372a2a6977cc4c724a421
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761274"
---
# <span data-ttu-id="94607-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="94607-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="94607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94607-102">SYNOPSIS</span></span>
<span data-ttu-id="94607-103">Bir sanal makineden SQL Server uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94607-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="94607-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94607-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94607-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="94607-105">DESCRIPTION</span></span>
<span data-ttu-id="94607-106">**Remove-AzVMSqlServerExtension** cmdlet 'i, bir AzureSQL Server uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94607-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="94607-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94607-107">EXAMPLES</span></span>

### <span data-ttu-id="94607-108">Örnek 1: SQL Server uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="94607-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="94607-109">Bu komut, ContosoVM22 adındaki sanal makineden SQL Server uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94607-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="94607-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94607-110">PARAMETERS</span></span>

### <span data-ttu-id="94607-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94607-111">-DefaultProfile</span></span>
<span data-ttu-id="94607-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94607-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94607-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="94607-113">-Name</span></span>
<span data-ttu-id="94607-114">Bu cmdlet 'in kaldırdığı uzantının SQL Server adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94607-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94607-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94607-115">-ResourceGroupName</span></span>
<span data-ttu-id="94607-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94607-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94607-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="94607-117">-VMName</span></span>
<span data-ttu-id="94607-118">Bu cmdlet 'in SQL Server uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94607-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94607-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94607-119">CommonParameters</span></span>
<span data-ttu-id="94607-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94607-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94607-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94607-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94607-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94607-122">INPUTS</span></span>

### <span data-ttu-id="94607-123">System. String</span><span class="sxs-lookup"><span data-stu-id="94607-123">System.String</span></span>

## <span data-ttu-id="94607-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94607-124">OUTPUTS</span></span>

### <span data-ttu-id="94607-125">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="94607-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="94607-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94607-126">NOTES</span></span>

## <span data-ttu-id="94607-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94607-127">RELATED LINKS</span></span>

[<span data-ttu-id="94607-128">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="94607-128">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="94607-129">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="94607-129">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


