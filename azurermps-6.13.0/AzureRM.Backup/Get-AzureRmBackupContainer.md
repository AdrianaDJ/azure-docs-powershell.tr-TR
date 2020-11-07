---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: e20276d8a2dfec8ffb39665e5122cfe4be74dc42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762492"
---
# <span data-ttu-id="ad2b9-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ad2b9-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="ad2b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad2b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2b9-103">Yedekleme kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad2b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad2b9-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad2b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad2b9-105">DESCRIPTION</span></span>
<span data-ttu-id="ad2b9-106">**Get-AzureRmBackupContainer** cmdlet 'ı Azure yedekleme kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>
<span data-ttu-id="ad2b9-107">**AzureBackupContainer** , veri kaynaklarını, korumalı öğeleri ve kurtarma noktalarını saklar.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="ad2b9-108">**AzureBackupContainer** aşağıdakilerden biri olabilir:</span><span class="sxs-lookup"><span data-stu-id="ad2b9-108">An **AzureBackupContainer** can be one of the following:</span></span> 
- <span data-ttu-id="ad2b9-109">Windows Server bilgisayarı</span><span class="sxs-lookup"><span data-stu-id="ad2b9-109">A Windows Server computer</span></span>
- <span data-ttu-id="ad2b9-110">Sistem Merkezi veri koruma Yöneticisi (SCDPM) sunucusu</span><span class="sxs-lookup"><span data-stu-id="ad2b9-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="ad2b9-111">Azure alt yapısı (IaaS) sanal makinesi yedekleme bir veri kaynağını veya öğeyi yedekleyebilmeniz için, bunu Azure yedekleme hizmeti ile tutan kapsayıcıyı kaydettirmelidir.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-111">An Azure infrastructure as a service (IaaS) virtual machine Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="ad2b9-112">Yedek verileri yedekleme kasasına göndermek için kapsayıcının kimliklerinin doğrulanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-112">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="ad2b9-113">Windows Server bilgisayarları ve SCDPM sunucuları için kayıt, sunucunun tam nitelikli etki alanı adıyla tutulur.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-113">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="ad2b9-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad2b9-114">EXAMPLES</span></span>

### <span data-ttu-id="ad2b9-115">Örnek 1: kasaya kaydedilen tüm sunucuları görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ad2b9-115">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="ad2b9-116">İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-116">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ad2b9-117">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-117">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="ad2b9-118">İkinci komut $Vault Windows 'un tür kapsayıcılarından tüm kapsayıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-118">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="ad2b9-119">Örnek 2: belirli bir kapsayıcıyı alma</span><span class="sxs-lookup"><span data-stu-id="ad2b9-119">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="ad2b9-120">Bu komut, DPMSERVER adlı kapsayıcıyı alır. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-120">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="ad2b9-121">Komut $Vault ve kapsayıcının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-121">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="ad2b9-122">Örnek 3: Tüm kaydedilen Azure sanal makinelerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ad2b9-122">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="ad2b9-123">Bu komut, $Vault 'daki kasadan kaydedilen sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-123">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="ad2b9-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad2b9-124">PARAMETERS</span></span>

### <span data-ttu-id="ad2b9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2b9-125">-DefaultProfile</span></span>
<span data-ttu-id="ad2b9-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ad2b9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad2b9-127">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2b9-127">-ManagedResourceGroupName</span></span>
<span data-ttu-id="ad2b9-128">Kapsayıcıyla ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-128">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="ad2b9-129">Bu ad, Register-AzureRmBackupContainer cmdlet 'inin *ServiceName* veya *resourcegroupname* parametresi için belirttiğiniz değerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-129">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2b9-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad2b9-130">-Name</span></span>
<span data-ttu-id="ad2b9-131">Bu cmdlet 'in aldığı kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-131">Specifies the name of the container that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2b9-132">-Durum</span><span class="sxs-lookup"><span data-stu-id="ad2b9-132">-Status</span></span>
<span data-ttu-id="ad2b9-133">Bu cmdlet 'in aldığı kapsayıcıların geçerli durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-133">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="ad2b9-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ad2b9-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad2b9-135">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="ad2b9-135">NotRegistered</span></span> 
- <span data-ttu-id="ad2b9-136">Kaydedilemedi</span><span class="sxs-lookup"><span data-stu-id="ad2b9-136">Registered</span></span> 
- <span data-ttu-id="ad2b9-137">Kaydedilmesi</span><span class="sxs-lookup"><span data-stu-id="ad2b9-137">Registering</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2b9-138">-Tür</span><span class="sxs-lookup"><span data-stu-id="ad2b9-138">-Type</span></span>
<span data-ttu-id="ad2b9-139">Bu cmdlet 'in aldığı kapsayıcıların türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-139">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2b9-140">-Kasa</span><span class="sxs-lookup"><span data-stu-id="ad2b9-140">-Vault</span></span>
<span data-ttu-id="ad2b9-141">Bu cmdlet 'in kapsayıcıları aldığı bir yedek Kasası belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-141">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="ad2b9-142">**Azurermbackupkasası** edinmek için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-142">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2b9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2b9-143">CommonParameters</span></span>
<span data-ttu-id="ad2b9-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2b9-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2b9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2b9-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad2b9-146">INPUTS</span></span>

### <span data-ttu-id="ad2b9-147">Microsoft. Azure. Commands. AzureBackup. modeller. Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="ad2b9-147">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="ad2b9-148">Parametreler: kasa (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad2b9-148">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="ad2b9-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad2b9-149">OUTPUTS</span></span>

### <span data-ttu-id="ad2b9-150">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ad2b9-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>

## <span data-ttu-id="ad2b9-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad2b9-151">NOTES</span></span>
* <span data-ttu-id="ad2b9-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ad2b9-152">None</span></span>

## <span data-ttu-id="ad2b9-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad2b9-153">RELATED LINKS</span></span>

[<span data-ttu-id="ad2b9-154">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="ad2b9-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ad2b9-155">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ad2b9-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="ad2b9-156">Unregister-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ad2b9-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


