---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: add399ca208cdcd1f1b4395523f8df43875ff451
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278484"
---
# <span data-ttu-id="f7d99-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f7d99-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="f7d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7d99-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d99-103">Bu komut, belirli bir kapsayıcıdaki veya tüm kaydedilmiş kapsayıcılardaki tüm korunabilir öğeleri alır.</span><span class="sxs-lookup"><span data-stu-id="f7d99-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="f7d99-104">Uygulama hiyerarşisinin tüm öğelerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="f7d99-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="f7d99-105">Örnek, kullanılabilirlik grubu gibi DBs ve bunların üst katman varlıklarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f7d99-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="f7d99-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7d99-106">SYNTAX</span></span>

### <span data-ttu-id="f7d99-107">NoFilterParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7d99-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7d99-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="f7d99-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7d99-109">Idparamset</span><span class="sxs-lookup"><span data-stu-id="f7d99-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7d99-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7d99-110">DESCRIPTION</span></span>
<span data-ttu-id="f7d99-111">**Get-Azrecoveryservicesbackupkorunabilir öğe** cmdlet 'inde, bir kapsayıcıdaki korunabilir öğelerin listesini ve öğelerin koruma durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="f7d99-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="f7d99-112">Azure kurtarma hizmetleri kasasına kaydedilen bir kapsayıcının korunabilir bir veya birden çok öğe olabilir.</span><span class="sxs-lookup"><span data-stu-id="f7d99-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="f7d99-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7d99-113">EXAMPLES</span></span>

### <span data-ttu-id="f7d99-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f7d99-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="f7d99-115">İlk komut MSSQL türünde kapsayıcıyı alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f7d99-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="f7d99-116">İkinci komut $Container yedek korunabilir öğesini alır ve $Item değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f7d99-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="f7d99-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7d99-117">PARAMETERS</span></span>

### <span data-ttu-id="f7d99-118">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="f7d99-118">-Container</span></span>
<span data-ttu-id="f7d99-119">Öğenin bulunduğu kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="f7d99-119">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d99-120">-DefaultProfile</span></span>
<span data-ttu-id="f7d99-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7d99-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d99-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="f7d99-122">-ItemType</span></span>
<span data-ttu-id="f7d99-123">Korunabilir öğe türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7d99-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="f7d99-124">İlgili değerler: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="f7d99-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemType
Parameter Sets: FilterParamSet, IdParamSet
Aliases:
Accepted values: SQLDataBase, SQLInstance, SQLAvailabilityGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d99-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="f7d99-125">-Name</span></span>
<span data-ttu-id="f7d99-126">Veritabanının, örneğin veya kullanılabilirlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7d99-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d99-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="f7d99-127">-ParentID</span></span>
<span data-ttu-id="f7d99-128">Bir örnek veya ağ üzerindeki ARM KIMLIĞI belirtildi.</span><span class="sxs-lookup"><span data-stu-id="f7d99-128">Specified the ARM ID of an Instance or AG.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d99-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f7d99-129">-ServerName</span></span>
<span data-ttu-id="f7d99-130">Öğenin ait olduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7d99-130">Specifies the name of the server to which the item belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d99-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f7d99-131">-VaultId</span></span>
<span data-ttu-id="f7d99-132">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f7d99-132">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d99-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="f7d99-133">-WorkloadType</span></span>
<span data-ttu-id="f7d99-134">Kaynağın iş yükü türü.</span><span class="sxs-lookup"><span data-stu-id="f7d99-134">Workload type of the resource.</span></span> <span data-ttu-id="f7d99-135">AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="f7d99-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d99-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d99-136">CommonParameters</span></span>
<span data-ttu-id="f7d99-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7d99-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d99-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f7d99-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d99-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7d99-139">INPUTS</span></span>

### <span data-ttu-id="f7d99-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="f7d99-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="f7d99-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f7d99-141">System.String</span></span>

## <span data-ttu-id="f7d99-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7d99-142">OUTPUTS</span></span>

### <span data-ttu-id="f7d99-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Koruyucutablotembase</span><span class="sxs-lookup"><span data-stu-id="f7d99-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="f7d99-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7d99-144">NOTES</span></span>

## <span data-ttu-id="f7d99-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7d99-145">RELATED LINKS</span></span>
