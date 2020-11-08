---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e63812f1972effd7956911861e5c6e07436fd4c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279385"
---
# <span data-ttu-id="6fed4-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6fed4-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="6fed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fed4-102">SYNOPSIS</span></span>
<span data-ttu-id="6fed4-103">Azure NetApp dosyalarını (ANF) sağlanan isteğe bağlı değiştiricilere göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6fed4-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="6fed4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fed4-104">SYNTAX</span></span>

### <span data-ttu-id="6fed4-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6fed4-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fed4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fed4-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fed4-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6fed4-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fed4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fed4-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fed4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fed4-109">DESCRIPTION</span></span>
<span data-ttu-id="6fed4-110">**Update-AzNetAppFilesPool** cmdlet 'i ANF havuzunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6fed4-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="6fed4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fed4-111">EXAMPLES</span></span>

### <span data-ttu-id="6fed4-112">Örnek 1: ANF havuzunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="6fed4-112">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="6fed4-113">Bu komut, "MyAnfPool" ANF havuzunu verilen boyut ve ServiceLevel 'e dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="6fed4-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="6fed4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fed4-114">PARAMETERS</span></span>

### <span data-ttu-id="6fed4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6fed4-115">-AccountName</span></span>
<span data-ttu-id="6fed4-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="6fed4-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fed4-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6fed4-117">-AccountObject</span></span>
<span data-ttu-id="6fed4-118">Güncelleştirilecek havuzu içeren hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="6fed4-118">The account object containing the pool to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fed4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fed4-119">-DefaultProfile</span></span>
<span data-ttu-id="6fed4-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fed4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fed4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fed4-121">-InputObject</span></span>
<span data-ttu-id="6fed4-122">Güncelleştirilecek havuz nesnesi</span><span class="sxs-lookup"><span data-stu-id="6fed4-122">The pool object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fed4-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="6fed4-123">-Location</span></span>
<span data-ttu-id="6fed4-124">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="6fed4-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fed4-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="6fed4-125">-Name</span></span>
<span data-ttu-id="6fed4-126">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="6fed4-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fed4-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="6fed4-127">-PoolSize</span></span>
<span data-ttu-id="6fed4-128">ANF havuzunun boyutu</span><span class="sxs-lookup"><span data-stu-id="6fed4-128">The size of the ANF pool</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fed4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fed4-129">-ResourceGroupName</span></span>
<span data-ttu-id="6fed4-130">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="6fed4-130">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fed4-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6fed4-131">-ResourceId</span></span>
<span data-ttu-id="6fed4-132">ANF havuzunun kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6fed4-132">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fed4-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="6fed4-133">-ServiceLevel</span></span>
<span data-ttu-id="6fed4-134">ANF havuzunun hizmet düzeyi</span><span class="sxs-lookup"><span data-stu-id="6fed4-134">The service level of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fed4-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6fed4-135">-Tag</span></span>
<span data-ttu-id="6fed4-136">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="6fed4-136">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fed4-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="6fed4-137">-Confirm</span></span>
<span data-ttu-id="6fed4-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6fed4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fed4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fed4-139">-WhatIf</span></span>
<span data-ttu-id="6fed4-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fed4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fed4-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6fed4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fed4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fed4-142">CommonParameters</span></span>
<span data-ttu-id="6fed4-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fed4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fed4-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6fed4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fed4-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fed4-145">INPUTS</span></span>

### <span data-ttu-id="6fed4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6fed4-146">System.String</span></span>

### <span data-ttu-id="6fed4-147">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6fed4-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="6fed4-148">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6fed4-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="6fed4-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fed4-149">OUTPUTS</span></span>

### <span data-ttu-id="6fed4-150">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6fed4-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="6fed4-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fed4-151">NOTES</span></span>

## <span data-ttu-id="6fed4-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fed4-152">RELATED LINKS</span></span>
