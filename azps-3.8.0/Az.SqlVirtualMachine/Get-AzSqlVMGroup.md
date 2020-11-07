---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937931"
---
# <span data-ttu-id="1f778-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="1f778-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="1f778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f778-102">SYNOPSIS</span></span>
<span data-ttu-id="1f778-103">Bir veya daha fazla SQL sanal makine grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="1f778-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="1f778-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f778-104">SYNTAX</span></span>

### <span data-ttu-id="1f778-105">Yalnızca Resourcegroup(varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1f778-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f778-106">Adlandır</span><span class="sxs-lookup"><span data-stu-id="1f778-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f778-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="1f778-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f778-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f778-108">DESCRIPTION</span></span>
<span data-ttu-id="1f778-109">Get-AzSqlVMGroup cmdlet bir veya birden çok SQL sanal makine grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="1f778-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="1f778-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f778-110">EXAMPLES</span></span>

### <span data-ttu-id="1f778-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1f778-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="1f778-112">Bu komut, geçerli abonelikteki tüm Azure SQL sanal makine grupları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="1f778-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="1f778-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1f778-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="1f778-114">Bu komut, ResourceGroup01 kaynak grubuna atanmış geçerli abonelikteki tüm Azure SQL sanal makine grupları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="1f778-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="1f778-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1f778-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="1f778-116">Bu komut, kaynak grubuna ResourceGroup01 atanan SQL sanal makine grubu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="1f778-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="1f778-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f778-117">PARAMETERS</span></span>

### <span data-ttu-id="1f778-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f778-118">-DefaultProfile</span></span>
<span data-ttu-id="1f778-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f778-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f778-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f778-120">-Name</span></span>
<span data-ttu-id="1f778-121">SQL sanal makine grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1f778-121">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f778-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f778-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f778-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1f778-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f778-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1f778-124">-ResourceId</span></span>
<span data-ttu-id="1f778-125">SQL sanal makine grubu kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1f778-125">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f778-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f778-126">CommonParameters</span></span>
<span data-ttu-id="1f778-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f778-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f778-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1f778-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f778-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f778-129">INPUTS</span></span>

### <span data-ttu-id="1f778-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1f778-130">System.String</span></span>

## <span data-ttu-id="1f778-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f778-131">OUTPUTS</span></span>

### <span data-ttu-id="1f778-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmgroupmodel</span><span class="sxs-lookup"><span data-stu-id="1f778-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="1f778-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f778-133">NOTES</span></span>

## <span data-ttu-id="1f778-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f778-134">RELATED LINKS</span></span>
