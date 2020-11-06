---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 83f697733d56ae7d99bc0b2660b5abbaca15a71f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594445"
---
# <span data-ttu-id="2c146-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2c146-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="2c146-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c146-102">SYNOPSIS</span></span>
<span data-ttu-id="2c146-103">Bir sanal makineden SQL Server uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2c146-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c146-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c146-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c146-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c146-105">DESCRIPTION</span></span>
<span data-ttu-id="2c146-106">**Remove-AzureRmVMSqlServerExtension** cmdlet 'i, bir AzureSQL sunucu uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2c146-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="2c146-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c146-107">EXAMPLES</span></span>

### <span data-ttu-id="2c146-108">Örnek 1: SQL Server uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="2c146-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="2c146-109">Bu komut, ContosoVM22 adındaki sanal makineden SQL Server uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2c146-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="2c146-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c146-110">PARAMETERS</span></span>

### <span data-ttu-id="2c146-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c146-111">-DefaultProfile</span></span>
<span data-ttu-id="2c146-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c146-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c146-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c146-113">-Name</span></span>
<span data-ttu-id="2c146-114">Bu cmdlet 'in kaldırdığı uzantının SQL Server adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c146-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2c146-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c146-115">-ResourceGroupName</span></span>
<span data-ttu-id="2c146-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c146-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2c146-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="2c146-117">-VMName</span></span>
<span data-ttu-id="2c146-118">Bu cmdlet 'in SQL Server uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c146-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="2c146-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c146-119">CommonParameters</span></span>
<span data-ttu-id="2c146-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c146-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c146-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c146-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c146-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c146-122">INPUTS</span></span>

### <span data-ttu-id="2c146-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2c146-123">System.String</span></span>

## <span data-ttu-id="2c146-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c146-124">OUTPUTS</span></span>

### <span data-ttu-id="2c146-125">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2c146-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2c146-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c146-126">NOTES</span></span>

## <span data-ttu-id="2c146-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c146-127">RELATED LINKS</span></span>

[<span data-ttu-id="2c146-128">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2c146-128">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="2c146-129">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2c146-129">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


