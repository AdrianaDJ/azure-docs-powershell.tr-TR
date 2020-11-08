---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: f061dc0f729709dee3bfe08bb22dba8d49a7f31b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107695"
---
# <span data-ttu-id="158ef-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="158ef-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="158ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="158ef-102">SYNOPSIS</span></span>

<span data-ttu-id="158ef-103">Yedekleme kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="158ef-103">Gets Backup containers.</span></span>

## <span data-ttu-id="158ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="158ef-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="158ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="158ef-105">DESCRIPTION</span></span>

<span data-ttu-id="158ef-106">**Get-AzRecoveryServicesBackupContainer** cmdlet 'i bir yedekleme kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="158ef-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="158ef-107">Yedekleme kapsayıcısı, yedek öğeler olarak modelli veri kaynaklarını saklar.</span><span class="sxs-lookup"><span data-stu-id="158ef-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="158ef-108">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="158ef-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="158ef-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="158ef-109">EXAMPLES</span></span>

### <span data-ttu-id="158ef-110">Örnek 1: belirli bir kapsayıcıyı alma</span><span class="sxs-lookup"><span data-stu-id="158ef-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="158ef-111">Bu komut, AzureVM türünde V2VM adlı kapsayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="158ef-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="158ef-112">Örnek 2: belirli bir türdeki tüm kapsayıcıları alma</span><span class="sxs-lookup"><span data-stu-id="158ef-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="158ef-113">Bu komut, Azure Yedekleme aracısı tarafından korunan tüm Windows kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="158ef-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="158ef-114">**Backupmanagementtype** parametresi yalnızca Windows kapsayıcıları için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="158ef-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="158ef-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="158ef-115">PARAMETERS</span></span>

### <span data-ttu-id="158ef-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="158ef-116">-BackupManagementType</span></span>

<span data-ttu-id="158ef-117">Korunan kaynakların sınıfı.</span><span class="sxs-lookup"><span data-stu-id="158ef-117">The class of resources being protected.</span></span> <span data-ttu-id="158ef-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="158ef-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="158ef-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="158ef-119">AzureVM</span></span>
- <span data-ttu-id="158ef-120">MARS</span><span class="sxs-lookup"><span data-stu-id="158ef-120">MARS</span></span>
- <span data-ttu-id="158ef-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="158ef-121">AzureWorkload</span></span>
- <span data-ttu-id="158ef-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="158ef-122">AzureStorage</span></span>

<span data-ttu-id="158ef-123">Bu parametre, MARS Aracısı veya diğer yedekleme altyapıları kullanılarak yedeklenen Windows makinelerini ayırt etmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="158ef-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="158ef-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="158ef-124">-ContainerType</span></span>

<span data-ttu-id="158ef-125">Yedekleme kapsayıcısı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="158ef-125">Specifies the backup container type.</span></span>
<span data-ttu-id="158ef-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="158ef-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="158ef-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="158ef-127">AzureVM</span></span>
- <span data-ttu-id="158ef-128">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="158ef-128">Windows</span></span>
- <span data-ttu-id="158ef-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="158ef-129">AzureSQL</span></span>
- <span data-ttu-id="158ef-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="158ef-130">AzureStorage</span></span>
- <span data-ttu-id="158ef-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="158ef-131">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="158ef-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158ef-132">-DefaultProfile</span></span>

<span data-ttu-id="158ef-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="158ef-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="158ef-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="158ef-134">-FriendlyName</span></span>

<span data-ttu-id="158ef-135">Alınacak kapsayıcının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="158ef-135">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="158ef-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="158ef-136">-ResourceGroupName</span></span>

<span data-ttu-id="158ef-137">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="158ef-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="158ef-138">Bu parametre yalnızca Azure sanal makinelerinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="158ef-138">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="158ef-139">-Durum</span><span class="sxs-lookup"><span data-stu-id="158ef-139">-Status</span></span>

<span data-ttu-id="158ef-140">Kapsayıcı kayıt durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="158ef-140">Specifies the container registration status.</span></span>
<span data-ttu-id="158ef-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="158ef-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="158ef-142">Kaydedilemedi</span><span class="sxs-lookup"><span data-stu-id="158ef-142">Registered</span></span>

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

### <span data-ttu-id="158ef-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="158ef-143">-VaultId</span></span>

<span data-ttu-id="158ef-144">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="158ef-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="158ef-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158ef-145">CommonParameters</span></span>
<span data-ttu-id="158ef-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="158ef-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158ef-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="158ef-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158ef-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="158ef-148">INPUTS</span></span>

### <span data-ttu-id="158ef-149">System. String</span><span class="sxs-lookup"><span data-stu-id="158ef-149">System.String</span></span>

## <span data-ttu-id="158ef-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="158ef-150">OUTPUTS</span></span>

### <span data-ttu-id="158ef-151">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="158ef-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="158ef-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="158ef-152">NOTES</span></span>

## <span data-ttu-id="158ef-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="158ef-153">RELATED LINKS</span></span>

[<span data-ttu-id="158ef-154">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="158ef-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="158ef-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="158ef-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="158ef-156">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="158ef-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
