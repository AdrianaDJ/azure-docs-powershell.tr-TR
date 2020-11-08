---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: 29fc27c16b8e084229134ed2389eab7685b1d43f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937252"
---
# <span data-ttu-id="f783d-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f783d-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="f783d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f783d-102">SYNOPSIS</span></span>
<span data-ttu-id="f783d-103">Yeni bir Azure NetApp dosyaları (ANF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f783d-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="f783d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f783d-104">SYNTAX</span></span>

### <span data-ttu-id="f783d-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f783d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f783d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f783d-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f783d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f783d-107">DESCRIPTION</span></span>
<span data-ttu-id="f783d-108">**New-AzNetAppFilesPool** cmdlet 'ı BIR ANF havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f783d-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="f783d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f783d-109">EXAMPLES</span></span>

### <span data-ttu-id="f783d-110">Örnek 1: ANF havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="f783d-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="f783d-111">Bu komut, "MyAnfAccount" hesabında yeni bir "MyAnfPool" oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f783d-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="f783d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f783d-112">PARAMETERS</span></span>

### <span data-ttu-id="f783d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f783d-113">-AccountName</span></span>
<span data-ttu-id="f783d-114">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="f783d-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="f783d-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="f783d-115">-AccountObject</span></span>
<span data-ttu-id="f783d-116">Yeni havuz nesnesinin hesabı</span><span class="sxs-lookup"><span data-stu-id="f783d-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="f783d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f783d-117">-DefaultProfile</span></span>
<span data-ttu-id="f783d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f783d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f783d-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="f783d-119">-Location</span></span>
<span data-ttu-id="f783d-120">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="f783d-120">The location of the resource</span></span>

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

### <span data-ttu-id="f783d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="f783d-121">-Name</span></span>
<span data-ttu-id="f783d-122">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="f783d-122">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f783d-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="f783d-123">-PoolSize</span></span>
<span data-ttu-id="f783d-124">ANF havuzunun boyutu</span><span class="sxs-lookup"><span data-stu-id="f783d-124">The size of the ANF pool</span></span>

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

### <span data-ttu-id="f783d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f783d-125">-ResourceGroupName</span></span>
<span data-ttu-id="f783d-126">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="f783d-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f783d-127">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="f783d-127">-ServiceLevel</span></span>
<span data-ttu-id="f783d-128">ANF havuzunun hizmet düzeyi</span><span class="sxs-lookup"><span data-stu-id="f783d-128">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="f783d-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f783d-129">-Tag</span></span>
<span data-ttu-id="f783d-130">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="f783d-130">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f783d-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="f783d-131">-Confirm</span></span>
<span data-ttu-id="f783d-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f783d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f783d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f783d-133">-WhatIf</span></span>
<span data-ttu-id="f783d-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f783d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f783d-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f783d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f783d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f783d-136">CommonParameters</span></span>
<span data-ttu-id="f783d-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f783d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f783d-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f783d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f783d-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f783d-139">INPUTS</span></span>

### <span data-ttu-id="f783d-140">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f783d-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="f783d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f783d-141">OUTPUTS</span></span>

### <span data-ttu-id="f783d-142">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f783d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="f783d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f783d-143">NOTES</span></span>

## <span data-ttu-id="f783d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f783d-144">RELATED LINKS</span></span>