---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 141c601b5a903462b15bbeb45d410db24608323f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751584"
---
# <span data-ttu-id="f5e8a-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="f5e8a-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="f5e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e8a-103">Var olan bir kusto veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="f5e8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5e8a-104">SYNTAX</span></span>

### <span data-ttu-id="f5e8a-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f5e8a-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5e8a-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f5e8a-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5e8a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f5e8a-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5e8a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5e8a-108">DESCRIPTION</span></span>
<span data-ttu-id="f5e8a-109">Var olan bir kusto veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="f5e8a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5e8a-110">EXAMPLES</span></span>

### <span data-ttu-id="f5e8a-111">Örnek 1-varolan bir kusto veritabanını adla silme</span><span class="sxs-lookup"><span data-stu-id="f5e8a-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="f5e8a-112">Yukarıdaki komut, "mykustodatabase" adlı kusto veritabanını "testrg" kaynak grubunda bulunan "mykustocluster" kümesinde siler.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="f5e8a-113">Örnek 2-yöneltme ile mevcut bir kusto veritabanını silme</span><span class="sxs-lookup"><span data-stu-id="f5e8a-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="f5e8a-114">Yukarıdaki komut, cmdlet 'i kullanarak "mykustodatabase" kaynak grubunda bulunan "mykustocluster" kümesindeki "" adlı kusto veritabanını alır `Get-AzKustoDatabase` ve sonra `Remove-AzKustoDatabase` da bunu silmek için sonucu yöneltin.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="f5e8a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5e8a-115">PARAMETERS</span></span>

### <span data-ttu-id="f5e8a-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f5e8a-116">-ClusterName</span></span>
<span data-ttu-id="f5e8a-117">Veritabanının bulunduğu kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-117">Name of the cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e8a-118">-DefaultProfile</span></span>
<span data-ttu-id="f5e8a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5e8a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5e8a-120">-InputObject</span></span>
<span data-ttu-id="f5e8a-121">Kusto veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-121">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e8a-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5e8a-122">-Name</span></span>
<span data-ttu-id="f5e8a-123">Kaldırılacak veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-123">Name of database to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e8a-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f5e8a-124">-PassThru</span></span>
<span data-ttu-id="f5e8a-125">Belirtilen veritabanının başarıyla askıya alınıp alınmadığını geri alma.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-125">Return whether the specified database was successfully suspended or not.</span></span>

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

### <span data-ttu-id="f5e8a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e8a-126">-ResourceGroupName</span></span>
<span data-ttu-id="f5e8a-127">Kümenin bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e8a-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f5e8a-128">-ResourceId</span></span>
<span data-ttu-id="f5e8a-129">Kusto veritabanı RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e8a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="f5e8a-130">-Confirm</span></span>
<span data-ttu-id="f5e8a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5e8a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5e8a-132">-WhatIf</span></span>
<span data-ttu-id="f5e8a-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5e8a-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5e8a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e8a-135">CommonParameters</span></span>
<span data-ttu-id="f5e8a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5e8a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e8a-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e8a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e8a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5e8a-138">INPUTS</span></span>

### <span data-ttu-id="f5e8a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f5e8a-139">System.String</span></span>

### <span data-ttu-id="f5e8a-140">Microsoft. Azure. Commands. kusto. modeller. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="f5e8a-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="f5e8a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5e8a-141">OUTPUTS</span></span>

### <span data-ttu-id="f5e8a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5e8a-142">System.Boolean</span></span>

## <span data-ttu-id="f5e8a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5e8a-143">NOTES</span></span>

## <span data-ttu-id="f5e8a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5e8a-144">RELATED LINKS</span></span>
