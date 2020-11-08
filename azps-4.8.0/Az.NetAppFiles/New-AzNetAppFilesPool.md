---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: f3b1a6180fb59b3c44942459e09a22a333fc9720
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109534"
---
# <span data-ttu-id="04f41-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="04f41-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="04f41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04f41-102">SYNOPSIS</span></span>
<span data-ttu-id="04f41-103">Yeni bir Azure NetApp dosyaları (ANF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04f41-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="04f41-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04f41-104">SYNTAX</span></span>

### <span data-ttu-id="04f41-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04f41-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f41-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04f41-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04f41-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="04f41-107">DESCRIPTION</span></span>
<span data-ttu-id="04f41-108">**New-AzNetAppFilesPool** cmdlet 'ı BIR ANF havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04f41-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="04f41-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04f41-109">EXAMPLES</span></span>

### <span data-ttu-id="04f41-110">Örnek 1: ANF havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="04f41-110">Example 1: Create an ANF pool</span></span>
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

<span data-ttu-id="04f41-111">Bu komut, "MyAnfAccount" hesabında yeni bir "MyAnfPool" oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04f41-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="04f41-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04f41-112">PARAMETERS</span></span>

### <span data-ttu-id="04f41-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="04f41-113">-AccountName</span></span>
<span data-ttu-id="04f41-114">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="04f41-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="04f41-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="04f41-115">-AccountObject</span></span>
<span data-ttu-id="04f41-116">Yeni havuz nesnesinin hesabı</span><span class="sxs-lookup"><span data-stu-id="04f41-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="04f41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f41-117">-DefaultProfile</span></span>
<span data-ttu-id="04f41-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04f41-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04f41-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="04f41-119">-Location</span></span>
<span data-ttu-id="04f41-120">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="04f41-120">The location of the resource</span></span>

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

### <span data-ttu-id="04f41-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="04f41-121">-Name</span></span>
<span data-ttu-id="04f41-122">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="04f41-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f41-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="04f41-123">-PoolSize</span></span>
<span data-ttu-id="04f41-124">ANF havuzunun boyutu</span><span class="sxs-lookup"><span data-stu-id="04f41-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f41-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04f41-125">-ResourceGroupName</span></span>
<span data-ttu-id="04f41-126">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="04f41-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="04f41-127">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="04f41-127">-ServiceLevel</span></span>
<span data-ttu-id="04f41-128">ANF havuzunun hizmet düzeyi</span><span class="sxs-lookup"><span data-stu-id="04f41-128">The service level of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f41-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="04f41-129">-Tag</span></span>
<span data-ttu-id="04f41-130">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="04f41-130">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="04f41-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="04f41-131">-Confirm</span></span>
<span data-ttu-id="04f41-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04f41-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04f41-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04f41-133">-WhatIf</span></span>
<span data-ttu-id="04f41-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04f41-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04f41-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04f41-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04f41-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f41-136">CommonParameters</span></span>
<span data-ttu-id="04f41-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04f41-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f41-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="04f41-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f41-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04f41-139">INPUTS</span></span>

### <span data-ttu-id="04f41-140">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="04f41-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="04f41-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04f41-141">OUTPUTS</span></span>

### <span data-ttu-id="04f41-142">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="04f41-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="04f41-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04f41-143">NOTES</span></span>

## <span data-ttu-id="04f41-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04f41-144">RELATED LINKS</span></span>
