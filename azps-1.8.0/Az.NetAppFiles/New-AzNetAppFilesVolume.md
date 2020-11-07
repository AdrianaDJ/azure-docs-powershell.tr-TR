---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: b742c8af0e8c36d07b2c608e74f0a02349502104
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760770"
---
# <span data-ttu-id="97630-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="97630-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="97630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97630-102">SYNOPSIS</span></span>
<span data-ttu-id="97630-103">Yeni bir Azure NetApp dosyaları (ANF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97630-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="97630-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97630-104">SYNTAX</span></span>

### <span data-ttu-id="97630-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97630-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97630-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97630-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97630-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="97630-107">DESCRIPTION</span></span>
<span data-ttu-id="97630-108">**Yeni-AzNetAppFilesVolume** cmdlet 'ı BIR ANF birimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97630-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="97630-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97630-109">EXAMPLES</span></span>

### <span data-ttu-id="97630-110">Örnek 1: ANF birimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="97630-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="97630-111">Bu komut, "MyAnfPool" havuzunda yeni ANF birimi "MyAnfVolume" oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97630-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="97630-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97630-112">PARAMETERS</span></span>

### <span data-ttu-id="97630-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="97630-113">-AccountName</span></span>
<span data-ttu-id="97630-114">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="97630-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="97630-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="97630-115">-CreationToken</span></span>
<span data-ttu-id="97630-116">Birim için benzersiz bir dosya yolu</span><span class="sxs-lookup"><span data-stu-id="97630-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="97630-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97630-117">-DefaultProfile</span></span>
<span data-ttu-id="97630-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97630-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97630-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="97630-119">-Location</span></span>
<span data-ttu-id="97630-120">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="97630-120">The location of the resource</span></span>

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

### <span data-ttu-id="97630-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="97630-121">-Name</span></span>
<span data-ttu-id="97630-122">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="97630-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97630-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="97630-123">-PoolName</span></span>
<span data-ttu-id="97630-124">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="97630-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="97630-125">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="97630-125">-PoolObject</span></span>
<span data-ttu-id="97630-126">Yeni birim için havuz</span><span class="sxs-lookup"><span data-stu-id="97630-126">The pool for the new volume object</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97630-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97630-127">-ResourceGroupName</span></span>
<span data-ttu-id="97630-128">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="97630-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="97630-129">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="97630-129">-ServiceLevel</span></span>
<span data-ttu-id="97630-130">ANF biriminin hizmet düzeyi</span><span class="sxs-lookup"><span data-stu-id="97630-130">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="97630-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="97630-131">-SubnetId</span></span>
<span data-ttu-id="97630-132">Atanmış bir alt ağ için Azure Resource URI 'SI</span><span class="sxs-lookup"><span data-stu-id="97630-132">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="97630-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="97630-133">-Tag</span></span>
<span data-ttu-id="97630-134">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="97630-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="97630-135">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="97630-135">-UsageThreshold</span></span>
<span data-ttu-id="97630-136">Bayt cinsinden bir dosya sistemi için izin verilen maksimum depolama kotası</span><span class="sxs-lookup"><span data-stu-id="97630-136">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="97630-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="97630-137">-Confirm</span></span>
<span data-ttu-id="97630-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97630-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97630-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97630-139">-WhatIf</span></span>
<span data-ttu-id="97630-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97630-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97630-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97630-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97630-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97630-142">CommonParameters</span></span>
<span data-ttu-id="97630-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97630-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="97630-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97630-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97630-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97630-145">INPUTS</span></span>

### <span data-ttu-id="97630-146">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="97630-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="97630-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97630-147">OUTPUTS</span></span>

### <span data-ttu-id="97630-148">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="97630-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="97630-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97630-149">NOTES</span></span>

## <span data-ttu-id="97630-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97630-150">RELATED LINKS</span></span>
