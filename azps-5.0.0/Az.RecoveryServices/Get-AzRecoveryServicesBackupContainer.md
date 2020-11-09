---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: f061dc0f729709dee3bfe08bb22dba8d49a7f31b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322444"
---
# <span data-ttu-id="f0bf9-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f0bf9-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="f0bf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0bf9-102">SYNOPSIS</span></span>

<span data-ttu-id="f0bf9-103">Yedekleme kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-103">Gets Backup containers.</span></span>

## <span data-ttu-id="f0bf9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0bf9-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0bf9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0bf9-105">DESCRIPTION</span></span>

<span data-ttu-id="f0bf9-106">**Get-AzRecoveryServicesBackupContainer** cmdlet 'i bir yedekleme kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="f0bf9-107">Yedekleme kapsayıcısı, yedek öğeler olarak modelli veri kaynaklarını saklar.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="f0bf9-108">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="f0bf9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0bf9-109">EXAMPLES</span></span>

### <span data-ttu-id="f0bf9-110">Örnek 1: belirli bir kapsayıcıyı alma</span><span class="sxs-lookup"><span data-stu-id="f0bf9-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="f0bf9-111">Bu komut, AzureVM türünde V2VM adlı kapsayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="f0bf9-112">Örnek 2: belirli bir türdeki tüm kapsayıcıları alma</span><span class="sxs-lookup"><span data-stu-id="f0bf9-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="f0bf9-113">Bu komut, Azure Yedekleme aracısı tarafından korunan tüm Windows kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="f0bf9-114">**Backupmanagementtype** parametresi yalnızca Windows kapsayıcıları için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="f0bf9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0bf9-115">PARAMETERS</span></span>

### <span data-ttu-id="f0bf9-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f0bf9-116">-BackupManagementType</span></span>

<span data-ttu-id="f0bf9-117">Korunan kaynakların sınıfı.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-117">The class of resources being protected.</span></span> <span data-ttu-id="f0bf9-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f0bf9-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f0bf9-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f0bf9-119">AzureVM</span></span>
- <span data-ttu-id="f0bf9-120">MARS</span><span class="sxs-lookup"><span data-stu-id="f0bf9-120">MARS</span></span>
- <span data-ttu-id="f0bf9-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="f0bf9-121">AzureWorkload</span></span>
- <span data-ttu-id="f0bf9-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f0bf9-122">AzureStorage</span></span>

<span data-ttu-id="f0bf9-123">Bu parametre, MARS Aracısı veya diğer yedekleme altyapıları kullanılarak yedeklenen Windows makinelerini ayırt etmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureWorkload, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bf9-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="f0bf9-124">-ContainerType</span></span>

<span data-ttu-id="f0bf9-125">Yedekleme kapsayıcısı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-125">Specifies the backup container type.</span></span>
<span data-ttu-id="f0bf9-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f0bf9-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f0bf9-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f0bf9-127">AzureVM</span></span>
- <span data-ttu-id="f0bf9-128">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="f0bf9-128">Windows</span></span>
- <span data-ttu-id="f0bf9-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="f0bf9-129">AzureSQL</span></span>
- <span data-ttu-id="f0bf9-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f0bf9-130">AzureStorage</span></span>
- <span data-ttu-id="f0bf9-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="f0bf9-131">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bf9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0bf9-132">-DefaultProfile</span></span>

<span data-ttu-id="f0bf9-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0bf9-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f0bf9-134">-FriendlyName</span></span>

<span data-ttu-id="f0bf9-135">Alınacak kapsayıcının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-135">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bf9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0bf9-136">-ResourceGroupName</span></span>

<span data-ttu-id="f0bf9-137">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="f0bf9-138">Bu parametre yalnızca Azure sanal makinelerinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-138">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bf9-139">-Durum</span><span class="sxs-lookup"><span data-stu-id="f0bf9-139">-Status</span></span>

<span data-ttu-id="f0bf9-140">Kapsayıcı kayıt durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-140">Specifies the container registration status.</span></span>
<span data-ttu-id="f0bf9-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f0bf9-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f0bf9-142">Kaydedilemedi</span><span class="sxs-lookup"><span data-stu-id="f0bf9-142">Registered</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bf9-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f0bf9-143">-VaultId</span></span>

<span data-ttu-id="f0bf9-144">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f0bf9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0bf9-145">CommonParameters</span></span>
<span data-ttu-id="f0bf9-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0bf9-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f0bf9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0bf9-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0bf9-148">INPUTS</span></span>

### <span data-ttu-id="f0bf9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f0bf9-149">System.String</span></span>

## <span data-ttu-id="f0bf9-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0bf9-150">OUTPUTS</span></span>

### <span data-ttu-id="f0bf9-151">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="f0bf9-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="f0bf9-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0bf9-152">NOTES</span></span>

## <span data-ttu-id="f0bf9-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0bf9-153">RELATED LINKS</span></span>

[<span data-ttu-id="f0bf9-154">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="f0bf9-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="f0bf9-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="f0bf9-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="f0bf9-156">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f0bf9-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
