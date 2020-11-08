---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273845"
---
# <span data-ttu-id="bbbed-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="bbbed-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="bbbed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbbed-102">SYNOPSIS</span></span>
<span data-ttu-id="bbbed-103">Bir veya birden çok SQL sanal makinesi alır.</span><span class="sxs-lookup"><span data-stu-id="bbbed-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="bbbed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbbed-104">SYNTAX</span></span>

### <span data-ttu-id="bbbed-105">Yalnızca Resourcegroup(varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bbbed-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbbed-106">Adlandır</span><span class="sxs-lookup"><span data-stu-id="bbbed-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bbbed-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="bbbed-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbbed-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbbed-108">DESCRIPTION</span></span>
<span data-ttu-id="bbbed-109">Get-AzSqlVM cmdlet bir veya birden çok SQL sanal makinesi alır.</span><span class="sxs-lookup"><span data-stu-id="bbbed-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="bbbed-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbbed-110">EXAMPLES</span></span>

### <span data-ttu-id="bbbed-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bbbed-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="bbbed-112">Bu komut, geçerli abonelikteki tüm Azure SQL sanal makineleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="bbbed-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="bbbed-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bbbed-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="bbbed-114">Bu komut, ResourceGroup01 kaynak grubuna atanmış geçerli abonelikteki tüm Azure SQL sanal makineleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="bbbed-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="bbbed-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="bbbed-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="bbbed-116">Bu komut, kaynak grubu ResourceGroup01 atanan SQL sanal makinesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="bbbed-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="bbbed-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbbed-117">PARAMETERS</span></span>

### <span data-ttu-id="bbbed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbbed-118">-DefaultProfile</span></span>
<span data-ttu-id="bbbed-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbbed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbbed-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="bbbed-120">-Name</span></span>
<span data-ttu-id="bbbed-121">SQL sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="bbbed-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="bbbed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbbed-122">-ResourceGroupName</span></span>
<span data-ttu-id="bbbed-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bbbed-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="bbbed-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bbbed-124">-ResourceId</span></span>
<span data-ttu-id="bbbed-125">SQL sanal makinesi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="bbbed-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="bbbed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbbed-126">CommonParameters</span></span>
<span data-ttu-id="bbbed-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbbed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbbed-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bbbed-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbbed-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbbed-129">INPUTS</span></span>

### <span data-ttu-id="bbbed-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bbbed-130">None</span></span>

## <span data-ttu-id="bbbed-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbbed-131">OUTPUTS</span></span>

### <span data-ttu-id="bbbed-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmmodel</span><span class="sxs-lookup"><span data-stu-id="bbbed-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="bbbed-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbbed-133">NOTES</span></span>

## <span data-ttu-id="bbbed-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbbed-134">RELATED LINKS</span></span>
