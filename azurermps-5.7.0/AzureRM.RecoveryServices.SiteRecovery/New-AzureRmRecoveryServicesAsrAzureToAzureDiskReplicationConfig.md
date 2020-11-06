---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 542e75ed0e6531f5778f9793b678b42f953c15d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573381"
---
# <span data-ttu-id="2c574-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="2c574-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="2c574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c574-102">SYNOPSIS</span></span>
<span data-ttu-id="2c574-103">Azure sanal makine disklerinin çoğaltılacağı bir disk eşleme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2c574-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c574-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c574-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c574-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c574-105">DESCRIPTION</span></span>
<span data-ttu-id="2c574-106">Bir Azure sanal makine diskini, diski çoğaltmak için kullanılacak önbellek depolama hesabına ve hedef depolama hesabına (kurtarma bölgesi) eşleyen bir disk eşleme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2c574-106">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="2c574-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c574-107">EXAMPLES</span></span>

### <span data-ttu-id="2c574-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c574-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="2c574-109">Çoğaltılacak Azure sanal makine disklerinin disk eşleme nesnesi oluşturma. Azure-Azure EnableDr ile ve yeniden korumada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2c574-109">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="2c574-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c574-110">PARAMETERS</span></span>

### <span data-ttu-id="2c574-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c574-111">-Confirm</span></span>
<span data-ttu-id="2c574-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c574-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c574-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c574-113">-DefaultProfile</span></span>
<span data-ttu-id="2c574-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c574-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c574-115">-Logstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="2c574-115">-LogStorageAccountId</span></span>
<span data-ttu-id="2c574-116">Çoğaltma günlüklerinin depolanacağı günlük veya önbellek hesap kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c574-116">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="2c574-117">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="2c574-117">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="2c574-118">Çoğaltılacak Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c574-118">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="2c574-119">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="2c574-119">-VhdUri</span></span>
<span data-ttu-id="2c574-120">Bu eşlemenin karşılık geldiği diskin VHD URI 'sini belirtin.</span><span class="sxs-lookup"><span data-stu-id="2c574-120">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="2c574-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c574-121">-WhatIf</span></span>
<span data-ttu-id="2c574-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c574-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c574-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c574-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c574-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c574-124">CommonParameters</span></span>
<span data-ttu-id="2c574-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c574-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c574-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c574-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c574-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c574-127">INPUTS</span></span>

### <span data-ttu-id="2c574-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2c574-128">None</span></span>

## <span data-ttu-id="2c574-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c574-129">OUTPUTS</span></span>

### <span data-ttu-id="2c574-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="2c574-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="2c574-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c574-131">NOTES</span></span>

## <span data-ttu-id="2c574-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c574-132">RELATED LINKS</span></span>
