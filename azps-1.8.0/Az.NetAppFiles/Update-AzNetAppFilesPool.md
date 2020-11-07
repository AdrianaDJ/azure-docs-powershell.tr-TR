---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 3dd02a2dc0cf7090ba2711b6155d25038397ab9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760759"
---
# <span data-ttu-id="a3fd9-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a3fd9-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="a3fd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="a3fd9-103">Bir Azure NetApp dosyaları (ANF) havuzunu yeni veri kümesiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a3fd9-103">Updates an Azure NetApp Files (ANF) pool with the new data set.</span></span>

## <span data-ttu-id="a3fd9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3fd9-104">SYNTAX</span></span>

### <span data-ttu-id="a3fd9-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3fd9-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3fd9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3fd9-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String>
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3fd9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3fd9-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -PoolSize <Int64> -ServiceLevel <String> -InputObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3fd9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3fd9-108">DESCRIPTION</span></span>
<span data-ttu-id="a3fd9-109">**Update-AzNetAppFilesPool** cmdlet 'i ANF havuzunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a3fd9-109">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="a3fd9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3fd9-110">EXAMPLES</span></span>

### <span data-ttu-id="a3fd9-111">Örnek 1: ANF havuzunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="a3fd9-111">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -ServiceLevel "Standard"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
ProvisioningState : Succeeded
```

<span data-ttu-id="a3fd9-112">Bu komut, "MyAnfPool" ANF havuzunu verilen boyut ve ServiceLevel 'e dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="a3fd9-112">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="a3fd9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3fd9-113">PARAMETERS</span></span>

### <span data-ttu-id="a3fd9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a3fd9-114">-AccountName</span></span>
<span data-ttu-id="a3fd9-115">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="a3fd9-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd9-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="a3fd9-116">-AccountObject</span></span>
<span data-ttu-id="a3fd9-117">Güncelleştirilecek havuzu içeren hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="a3fd9-117">The account object containing the pool to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3fd9-118">-DefaultProfile</span></span>
<span data-ttu-id="a3fd9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3fd9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3fd9-120">-InputObject</span></span>
<span data-ttu-id="a3fd9-121">Güncelleştirilecek havuz nesnesi</span><span class="sxs-lookup"><span data-stu-id="a3fd9-121">The pool object to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd9-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="a3fd9-122">-Location</span></span>
<span data-ttu-id="a3fd9-123">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="a3fd9-123">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd9-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3fd9-124">-Name</span></span>
<span data-ttu-id="a3fd9-125">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="a3fd9-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd9-126">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="a3fd9-126">-PoolSize</span></span>
<span data-ttu-id="a3fd9-127">ANF havuzunun boyutu</span><span class="sxs-lookup"><span data-stu-id="a3fd9-127">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3fd9-128">-ResourceGroupName</span></span>
<span data-ttu-id="a3fd9-129">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="a3fd9-129">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd9-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="a3fd9-130">-ServiceLevel</span></span>
<span data-ttu-id="a3fd9-131">ANF havuzunun hizmet düzeyi</span><span class="sxs-lookup"><span data-stu-id="a3fd9-131">The service level of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd9-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3fd9-132">-Confirm</span></span>
<span data-ttu-id="a3fd9-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3fd9-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3fd9-134">-WhatIf</span></span>
<span data-ttu-id="a3fd9-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3fd9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3fd9-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3fd9-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fd9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3fd9-137">CommonParameters</span></span>
<span data-ttu-id="a3fd9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3fd9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a3fd9-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3fd9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3fd9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3fd9-140">INPUTS</span></span>

### <span data-ttu-id="a3fd9-141">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a3fd9-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="a3fd9-142">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a3fd9-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="a3fd9-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3fd9-143">OUTPUTS</span></span>

### <span data-ttu-id="a3fd9-144">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a3fd9-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="a3fd9-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3fd9-145">NOTES</span></span>

## <span data-ttu-id="a3fd9-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3fd9-146">RELATED LINKS</span></span>
