---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325324"
---
# <span data-ttu-id="924b0-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="924b0-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="924b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="924b0-102">SYNOPSIS</span></span>
<span data-ttu-id="924b0-103">Bir sanal makineden SQL Server uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="924b0-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="924b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="924b0-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="924b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="924b0-105">DESCRIPTION</span></span>
<span data-ttu-id="924b0-106">**Remove-AzVMSqlServerExtension** cmdlet 'i, bir AzureSQL Server uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="924b0-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="924b0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="924b0-107">EXAMPLES</span></span>

### <span data-ttu-id="924b0-108">Örnek 1: SQL Server uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="924b0-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="924b0-109">Bu komut, ContosoVM22 adındaki sanal makineden SQL Server uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="924b0-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="924b0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="924b0-110">PARAMETERS</span></span>

### <span data-ttu-id="924b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924b0-111">-DefaultProfile</span></span>
<span data-ttu-id="924b0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="924b0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="924b0-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="924b0-113">-Name</span></span>
<span data-ttu-id="924b0-114">Bu cmdlet 'in kaldırdığı uzantının SQL Server adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="924b0-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="924b0-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="924b0-115">-NoWait</span></span>
<span data-ttu-id="924b0-116">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="924b0-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="924b0-117">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="924b0-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="924b0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="924b0-118">-ResourceGroupName</span></span>
<span data-ttu-id="924b0-119">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="924b0-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="924b0-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="924b0-120">-VMName</span></span>
<span data-ttu-id="924b0-121">Bu cmdlet 'in SQL Server uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="924b0-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="924b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924b0-122">CommonParameters</span></span>
<span data-ttu-id="924b0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="924b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924b0-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="924b0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924b0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="924b0-125">INPUTS</span></span>

### <span data-ttu-id="924b0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="924b0-126">System.String</span></span>

## <span data-ttu-id="924b0-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="924b0-127">OUTPUTS</span></span>

### <span data-ttu-id="924b0-128">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="924b0-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="924b0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="924b0-129">NOTES</span></span>

## <span data-ttu-id="924b0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="924b0-130">RELATED LINKS</span></span>

[<span data-ttu-id="924b0-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="924b0-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="924b0-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="924b0-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


