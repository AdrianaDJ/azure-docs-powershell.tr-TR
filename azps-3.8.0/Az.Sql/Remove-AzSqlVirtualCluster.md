---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098638"
---
# <span data-ttu-id="a5ada-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="a5ada-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="a5ada-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5ada-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ada-103">Azure SQL sanal kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a5ada-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="a5ada-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5ada-104">SYNTAX</span></span>

### <span data-ttu-id="a5ada-105">Removevirtualclusterfrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5ada-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ada-106">Removevirtualclusterfrolaurestarvirtualclusterdefinition</span><span class="sxs-lookup"><span data-stu-id="a5ada-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ada-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a5ada-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5ada-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5ada-108">DESCRIPTION</span></span>
<span data-ttu-id="a5ada-109">**Remove-AzSqlVirtualCluster** cmdlet 'ı BIR Azure SQL sanal kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a5ada-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="a5ada-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5ada-110">EXAMPLES</span></span>

### <span data-ttu-id="a5ada-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5ada-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="a5ada-112">Bu komut, kaynak grubuna atanmış VirtualCluster1 adındaki sanal kümeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a5ada-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="a5ada-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5ada-113">PARAMETERS</span></span>

### <span data-ttu-id="a5ada-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="a5ada-114">-AsJob</span></span>
<span data-ttu-id="a5ada-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a5ada-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5ada-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ada-116">-DefaultProfile</span></span>
<span data-ttu-id="a5ada-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5ada-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5ada-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5ada-118">-InputObject</span></span>
<span data-ttu-id="a5ada-119">Kaldırılacak örnek nesnesi</span><span class="sxs-lookup"><span data-stu-id="a5ada-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5ada-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5ada-120">-Name</span></span>
<span data-ttu-id="a5ada-121">Sanal kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="a5ada-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ada-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ada-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5ada-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a5ada-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ada-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a5ada-124">-ResourceId</span></span>
<span data-ttu-id="a5ada-125">Kaldırılacak örnek nesnenin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a5ada-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5ada-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5ada-126">-Confirm</span></span>
<span data-ttu-id="a5ada-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5ada-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ada-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5ada-128">-WhatIf</span></span>
<span data-ttu-id="a5ada-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5ada-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5ada-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5ada-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ada-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ada-131">CommonParameters</span></span>
<span data-ttu-id="a5ada-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5ada-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ada-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a5ada-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ada-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5ada-134">INPUTS</span></span>

### <span data-ttu-id="a5ada-135">Microsoft. Azure. Commands. Sql. Virtu</span><span class="sxs-lookup"><span data-stu-id="a5ada-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="a5ada-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a5ada-136">System.String</span></span>

## <span data-ttu-id="a5ada-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5ada-137">OUTPUTS</span></span>

### <span data-ttu-id="a5ada-138">Microsoft. Azure. Commands. Sql. Virtu</span><span class="sxs-lookup"><span data-stu-id="a5ada-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="a5ada-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5ada-139">NOTES</span></span>

## <span data-ttu-id="a5ada-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5ada-140">RELATED LINKS</span></span>
