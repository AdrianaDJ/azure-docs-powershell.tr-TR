---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937930"
---
# <span data-ttu-id="2beac-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="2beac-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="2beac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2beac-102">SYNOPSIS</span></span>
<span data-ttu-id="2beac-103">Bir veya birden çok SQL sanal makinesi alır.</span><span class="sxs-lookup"><span data-stu-id="2beac-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="2beac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2beac-104">SYNTAX</span></span>

### <span data-ttu-id="2beac-105">Yalnızca Resourcegroup(varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2beac-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2beac-106">Adlandır</span><span class="sxs-lookup"><span data-stu-id="2beac-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2beac-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="2beac-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2beac-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2beac-108">DESCRIPTION</span></span>
<span data-ttu-id="2beac-109">Get-AzSqlVM cmdlet bir veya birden çok SQL sanal makinesi alır.</span><span class="sxs-lookup"><span data-stu-id="2beac-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="2beac-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2beac-110">EXAMPLES</span></span>

### <span data-ttu-id="2beac-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2beac-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="2beac-112">Bu komut, geçerli abonelikteki tüm Azure SQL sanal makineleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2beac-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="2beac-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2beac-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="2beac-114">Bu komut, ResourceGroup01 kaynak grubuna atanmış geçerli abonelikteki tüm Azure SQL sanal makineleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2beac-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="2beac-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2beac-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="2beac-116">Bu komut, kaynak grubu ResourceGroup01 atanan SQL sanal makinesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2beac-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="2beac-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2beac-117">PARAMETERS</span></span>

### <span data-ttu-id="2beac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2beac-118">-DefaultProfile</span></span>
<span data-ttu-id="2beac-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2beac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2beac-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="2beac-120">-Name</span></span>
<span data-ttu-id="2beac-121">SQL sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="2beac-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2beac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2beac-122">-ResourceGroupName</span></span>
<span data-ttu-id="2beac-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2beac-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2beac-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2beac-124">-ResourceId</span></span>
<span data-ttu-id="2beac-125">SQL sanal makinesi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2beac-125">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2beac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2beac-126">CommonParameters</span></span>
<span data-ttu-id="2beac-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2beac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2beac-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2beac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2beac-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2beac-129">INPUTS</span></span>

### <span data-ttu-id="2beac-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2beac-130">None</span></span>

## <span data-ttu-id="2beac-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2beac-131">OUTPUTS</span></span>

### <span data-ttu-id="2beac-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmmodel</span><span class="sxs-lookup"><span data-stu-id="2beac-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="2beac-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2beac-133">NOTES</span></span>

## <span data-ttu-id="2beac-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2beac-134">RELATED LINKS</span></span>
