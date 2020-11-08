---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280069"
---
# <span data-ttu-id="89b0b-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="89b0b-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="89b0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="89b0b-103">Bir Azure Site kurtarma yapısı ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="89b0b-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="89b0b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89b0b-104">SYNTAX</span></span>

### <span data-ttu-id="89b0b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89b0b-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="89b0b-106">Al</span><span class="sxs-lookup"><span data-stu-id="89b0b-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="89b0b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="89b0b-107">DESCRIPTION</span></span>
<span data-ttu-id="89b0b-108">Bir Azure Site kurtarma yapısı ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="89b0b-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="89b0b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89b0b-109">EXAMPLES</span></span>

### <span data-ttu-id="89b0b-110">Örnek 1: kaynak grubuna ve kasa adına göre tüm yapıları alma</span><span class="sxs-lookup"><span data-stu-id="89b0b-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="89b0b-111">Kaynak grubundaki ve kasadaki tüm yapıları alma</span><span class="sxs-lookup"><span data-stu-id="89b0b-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="89b0b-112">Örnek 2: kaynak grubuna göre doku alma, kasa adı ve doku adı</span><span class="sxs-lookup"><span data-stu-id="89b0b-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="89b0b-113">Belirli bir doku alma</span><span class="sxs-lookup"><span data-stu-id="89b0b-113">Get a specific fabric</span></span>

## <span data-ttu-id="89b0b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89b0b-114">PARAMETERS</span></span>

### <span data-ttu-id="89b0b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b0b-115">-DefaultProfile</span></span>
<span data-ttu-id="89b0b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89b0b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b0b-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="89b0b-117">-FabricName</span></span>
<span data-ttu-id="89b0b-118">Doku adı.</span><span class="sxs-lookup"><span data-stu-id="89b0b-118">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b0b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89b0b-119">-ResourceGroupName</span></span>
<span data-ttu-id="89b0b-120">Kurtarma Hizmetleri kasasındaki kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="89b0b-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="89b0b-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="89b0b-121">-ResourceName</span></span>
<span data-ttu-id="89b0b-122">Kurtarma Hizmetleri kasasındaki adı.</span><span class="sxs-lookup"><span data-stu-id="89b0b-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="89b0b-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="89b0b-123">-SubscriptionId</span></span>
<span data-ttu-id="89b0b-124">Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="89b0b-124">The subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b0b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b0b-125">CommonParameters</span></span>
<span data-ttu-id="89b0b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89b0b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b0b-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="89b0b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b0b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89b0b-128">INPUTS</span></span>

## <span data-ttu-id="89b0b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89b0b-129">OUTPUTS</span></span>

### <span data-ttu-id="89b0b-130">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıfabrıc</span><span class="sxs-lookup"><span data-stu-id="89b0b-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="89b0b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89b0b-131">NOTES</span></span>

<span data-ttu-id="89b0b-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="89b0b-132">ALIASES</span></span>

## <span data-ttu-id="89b0b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89b0b-133">RELATED LINKS</span></span>

