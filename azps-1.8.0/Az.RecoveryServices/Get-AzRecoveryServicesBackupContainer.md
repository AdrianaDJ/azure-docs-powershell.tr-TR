---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 73438a3f294aaece7c4649f53559311d95ef4aa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759714"
---
# <span data-ttu-id="ac4a6-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ac4a6-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="ac4a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac4a6-102">SYNOPSIS</span></span>
<span data-ttu-id="ac4a6-103">Yedekleme kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-103">Gets Backup containers.</span></span>

## <span data-ttu-id="ac4a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac4a6-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac4a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac4a6-105">DESCRIPTION</span></span>
<span data-ttu-id="ac4a6-106">**Get-AzRecoveryServicesBackupContainer** cmdlet 'i bir yedekleme kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="ac4a6-107">Yedekleme kapsayıcısı, yedek öğeler olarak modelli veri kaynaklarını saklar.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="ac4a6-108">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-108">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ac4a6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac4a6-109">EXAMPLES</span></span>

### <span data-ttu-id="ac4a6-110">Örnek 1: belirli bir kapsayıcıyı alma</span><span class="sxs-lookup"><span data-stu-id="ac4a6-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="ac4a6-111">Bu komut, AzureVM türünde V2VM adlı kapsayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="ac4a6-112">Örnek 2: belirli bir türdeki tüm kapsayıcıları alma</span><span class="sxs-lookup"><span data-stu-id="ac4a6-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="ac4a6-113">Bu komut, Azure Yedekleme aracısı tarafından korunan tüm Windows kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="ac4a6-114">*Backupmanagementtype* parametresi yalnızca Windows kapsayıcıları için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="ac4a6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac4a6-115">PARAMETERS</span></span>

### <span data-ttu-id="ac4a6-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ac4a6-116">-BackupManagementType</span></span>
<span data-ttu-id="ac4a6-117">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-117">Specifies the backup management type.</span></span>
<span data-ttu-id="ac4a6-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ac4a6-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ac4a6-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ac4a6-119">AzureVM</span></span>
- <span data-ttu-id="ac4a6-120">MARS</span><span class="sxs-lookup"><span data-stu-id="ac4a6-120">MARS</span></span>
- <span data-ttu-id="ac4a6-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="ac4a6-121">AzureSQL</span></span>
- <span data-ttu-id="ac4a6-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="ac4a6-122">AzureStorage</span></span>

<span data-ttu-id="ac4a6-123">Bu parametre, MARS Aracısı veya diğer yedekleme altyapıları kullanılarak yedeklenen Windows makinelerini ayırt etmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="ac4a6-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="ac4a6-124">-ContainerType</span></span>
<span data-ttu-id="ac4a6-125">Yedekleme kapsayıcısı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-125">Specifies the backup container type.</span></span>
<span data-ttu-id="ac4a6-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ac4a6-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ac4a6-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ac4a6-127">AzureVM</span></span> 
- <span data-ttu-id="ac4a6-128">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="ac4a6-128">Windows</span></span>
- <span data-ttu-id="ac4a6-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="ac4a6-129">AzureSQL</span></span>
- <span data-ttu-id="ac4a6-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="ac4a6-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac4a6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac4a6-131">-DefaultProfile</span></span>
<span data-ttu-id="ac4a6-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac4a6-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ac4a6-133">-FriendlyName</span></span>
<span data-ttu-id="ac4a6-134">Alınacak kapsayıcının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="ac4a6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac4a6-135">-ResourceGroupName</span></span>
<span data-ttu-id="ac4a6-136">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="ac4a6-137">Bu parametre yalnızca Azure sanal makinelerinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-137">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="ac4a6-138">-Durum</span><span class="sxs-lookup"><span data-stu-id="ac4a6-138">-Status</span></span>
<span data-ttu-id="ac4a6-139">Kapsayıcı kayıt durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-139">Specifies the container registration status.</span></span>
<span data-ttu-id="ac4a6-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ac4a6-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ac4a6-141">Kaydedilemedi</span><span class="sxs-lookup"><span data-stu-id="ac4a6-141">Registered</span></span>

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

### <span data-ttu-id="ac4a6-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ac4a6-142">-VaultId</span></span>
<span data-ttu-id="ac4a6-143">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ac4a6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac4a6-144">CommonParameters</span></span>
<span data-ttu-id="ac4a6-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac4a6-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac4a6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac4a6-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac4a6-147">INPUTS</span></span>

### <span data-ttu-id="ac4a6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ac4a6-148">System.String</span></span>

## <span data-ttu-id="ac4a6-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac4a6-149">OUTPUTS</span></span>

### <span data-ttu-id="ac4a6-150">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="ac4a6-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="ac4a6-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac4a6-151">NOTES</span></span>

## <span data-ttu-id="ac4a6-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac4a6-152">RELATED LINKS</span></span>

[<span data-ttu-id="ac4a6-153">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ac4a6-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="ac4a6-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="ac4a6-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="ac4a6-155">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ac4a6-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

