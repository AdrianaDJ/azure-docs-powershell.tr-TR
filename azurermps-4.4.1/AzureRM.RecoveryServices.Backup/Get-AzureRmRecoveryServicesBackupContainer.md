---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: e6b0633b43bc93c516c9c5b6f4872ecbd6d68520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764535"
---
# <span data-ttu-id="12220-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="12220-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="12220-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12220-102">SYNOPSIS</span></span>
<span data-ttu-id="12220-103">Yedekleme kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="12220-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12220-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12220-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12220-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12220-105">DESCRIPTION</span></span>
<span data-ttu-id="12220-106">**Get-AzureRmRecoveryServicesBackupContainer** cmdlet 'i bir yedekleme kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="12220-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="12220-107">Yedekleme kapsayıcısı, yedek öğeler olarak modelli veri kaynaklarını saklar.</span><span class="sxs-lookup"><span data-stu-id="12220-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>

<span data-ttu-id="12220-108">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12220-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="12220-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12220-109">EXAMPLES</span></span>

### <span data-ttu-id="12220-110">Örnek 1: belirli bir kapsayıcıyı alma</span><span class="sxs-lookup"><span data-stu-id="12220-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="12220-111">Bu komut, AzureVM türünde V2VM adlı kapsayıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="12220-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="12220-112">Örnek 2: belirli bir türdeki tüm kapsayıcıları alma</span><span class="sxs-lookup"><span data-stu-id="12220-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="12220-113">Bu komut, Azure Yedekleme aracısı tarafından korunan tüm Windows kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="12220-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="12220-114">*Backupmanagementtype* parametresi yalnızca Windows kapsayıcıları için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="12220-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="12220-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12220-115">PARAMETERS</span></span>

### <span data-ttu-id="12220-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="12220-116">-BackupManagementType</span></span>
<span data-ttu-id="12220-117">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="12220-117">Specifies the backup management type.</span></span>
<span data-ttu-id="12220-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="12220-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="12220-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="12220-119">AzureVM</span></span>
- <span data-ttu-id="12220-120">MARS</span><span class="sxs-lookup"><span data-stu-id="12220-120">MARS</span></span>
- <span data-ttu-id="12220-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="12220-121">AzureSQL</span></span>

<span data-ttu-id="12220-122">Bu parametre, MARS Aracısı veya diğer yedekleme altyapıları kullanılarak yedeklenen Windows makinelerini ayırt etmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12220-122">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, AzureSQL

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12220-123">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="12220-123">-ContainerType</span></span>
<span data-ttu-id="12220-124">Yedekleme kapsayıcısı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="12220-124">Specifies the backup container type.</span></span>
<span data-ttu-id="12220-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="12220-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="12220-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="12220-126">AzureVM</span></span> 
- <span data-ttu-id="12220-127">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="12220-127">Windows</span></span>
- <span data-ttu-id="12220-128">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="12220-128">AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, Windows, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12220-129">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="12220-129">-FriendlyName</span></span>
<span data-ttu-id="12220-130">Alınacak kapsayıcının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12220-130">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="12220-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="12220-131">-Name</span></span>
<span data-ttu-id="12220-132">Alınacak kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12220-132">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="12220-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12220-133">-ResourceGroupName</span></span>
<span data-ttu-id="12220-134">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12220-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="12220-135">Bu parametre yalnızca Azure sanal makinelerinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12220-135">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="12220-136">-Durum</span><span class="sxs-lookup"><span data-stu-id="12220-136">-Status</span></span>
<span data-ttu-id="12220-137">Kapsayıcı kayıt durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="12220-137">Specifies the container registration status.</span></span>
<span data-ttu-id="12220-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="12220-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="12220-139">Kaydedilemedi</span><span class="sxs-lookup"><span data-stu-id="12220-139">Registered</span></span>

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

### <span data-ttu-id="12220-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12220-140">-DefaultProfile</span></span>
<span data-ttu-id="12220-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12220-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12220-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12220-142">CommonParameters</span></span>
<span data-ttu-id="12220-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12220-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12220-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12220-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12220-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12220-145">INPUTS</span></span>

## <span data-ttu-id="12220-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12220-146">OUTPUTS</span></span>

### <span data-ttu-id="12220-147">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="12220-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="12220-148">System. Koleksiyonlar. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase]</span><span class="sxs-lookup"><span data-stu-id="12220-148">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase]</span></span>

## <span data-ttu-id="12220-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12220-149">NOTES</span></span>

## <span data-ttu-id="12220-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12220-150">RELATED LINKS</span></span>

[<span data-ttu-id="12220-151">Get-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="12220-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="12220-152">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="12220-152">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="12220-153">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="12220-153">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


