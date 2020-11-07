---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c47c3e51d970302281af5a7ae3a6175f4af79739
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763817"
---
# <span data-ttu-id="f8704-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f8704-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="f8704-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8704-102">SYNOPSIS</span></span>
<span data-ttu-id="f8704-103">Yedekleme kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f8704-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8704-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8704-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8704-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8704-105">DESCRIPTION</span></span>
<span data-ttu-id="f8704-106">**Get-AzureRmRecoveryServicesBackupContainer** cmdlet 'i bir yedekleme kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="f8704-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="f8704-107">Yedekleme kapsayıcısı, yedek öğeler olarak modelli veri kaynaklarını saklar.</span><span class="sxs-lookup"><span data-stu-id="f8704-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="f8704-108">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f8704-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f8704-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8704-109">EXAMPLES</span></span>

### <span data-ttu-id="f8704-110">Örnek 1: belirli bir kapsayıcıyı alma</span><span class="sxs-lookup"><span data-stu-id="f8704-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="f8704-111">Bu komut, AzureVM türünde V2VM adlı kapsayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="f8704-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="f8704-112">Örnek 2: belirli bir türdeki tüm kapsayıcıları alma</span><span class="sxs-lookup"><span data-stu-id="f8704-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="f8704-113">Bu komut, Azure Yedekleme aracısı tarafından korunan tüm Windows kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f8704-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="f8704-114">*Backupmanagementtype* parametresi yalnızca Windows kapsayıcıları için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f8704-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="f8704-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8704-115">PARAMETERS</span></span>

### <span data-ttu-id="f8704-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f8704-116">-BackupManagementType</span></span>
<span data-ttu-id="f8704-117">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8704-117">Specifies the backup management type.</span></span>
<span data-ttu-id="f8704-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f8704-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f8704-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f8704-119">AzureVM</span></span>
- <span data-ttu-id="f8704-120">MARS</span><span class="sxs-lookup"><span data-stu-id="f8704-120">MARS</span></span>
- <span data-ttu-id="f8704-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="f8704-121">AzureSQL</span></span>
- <span data-ttu-id="f8704-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f8704-122">AzureStorage</span></span>

<span data-ttu-id="f8704-123">Bu parametre, MARS Aracısı veya diğer yedekleme altyapıları kullanılarak yedeklenen Windows makinelerini ayırt etmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f8704-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureSQL, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8704-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="f8704-124">-ContainerType</span></span>
<span data-ttu-id="f8704-125">Yedekleme kapsayıcısı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8704-125">Specifies the backup container type.</span></span>
<span data-ttu-id="f8704-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f8704-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f8704-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f8704-127">AzureVM</span></span> 
- <span data-ttu-id="f8704-128">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="f8704-128">Windows</span></span>
- <span data-ttu-id="f8704-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="f8704-129">AzureSQL</span></span>
- <span data-ttu-id="f8704-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f8704-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8704-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8704-131">-DefaultProfile</span></span>
<span data-ttu-id="f8704-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8704-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8704-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f8704-133">-FriendlyName</span></span>
<span data-ttu-id="f8704-134">Alınacak kapsayıcının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8704-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="f8704-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8704-135">-Name</span></span>
<span data-ttu-id="f8704-136">Alınacak kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8704-136">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="f8704-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8704-137">-ResourceGroupName</span></span>
<span data-ttu-id="f8704-138">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8704-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="f8704-139">Bu parametre yalnızca Azure sanal makinelerinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f8704-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="f8704-140">-Durum</span><span class="sxs-lookup"><span data-stu-id="f8704-140">-Status</span></span>
<span data-ttu-id="f8704-141">Kapsayıcı kayıt durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8704-141">Specifies the container registration status.</span></span>
<span data-ttu-id="f8704-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f8704-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f8704-143">Kaydedilemedi</span><span class="sxs-lookup"><span data-stu-id="f8704-143">Registered</span></span>

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

### <span data-ttu-id="f8704-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f8704-144">-VaultId</span></span>
<span data-ttu-id="f8704-145">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f8704-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f8704-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8704-146">CommonParameters</span></span>
<span data-ttu-id="f8704-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8704-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8704-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8704-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8704-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8704-149">INPUTS</span></span>

### <span data-ttu-id="f8704-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f8704-150">System.String</span></span>
<span data-ttu-id="f8704-151">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f8704-151">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="f8704-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8704-152">OUTPUTS</span></span>

### <span data-ttu-id="f8704-153">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="f8704-153">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="f8704-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8704-154">NOTES</span></span>

## <span data-ttu-id="f8704-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8704-155">RELATED LINKS</span></span>

[<span data-ttu-id="f8704-156">Get-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="f8704-156">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="f8704-157">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="f8704-157">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="f8704-158">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f8704-158">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


