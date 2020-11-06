---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: a6415d941646f335ba7cae4fc2aab39d75000ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591163"
---
# <span data-ttu-id="ad064-101">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ad064-101">New-AzureRmBackupVault</span></span>

## <span data-ttu-id="ad064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad064-102">SYNOPSIS</span></span>
<span data-ttu-id="ad064-103">Yedek Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad064-103">Creates a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad064-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad064-104">SYNTAX</span></span>

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad064-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad064-105">DESCRIPTION</span></span>
<span data-ttu-id="ad064-106">**New-Azurermbackupkasa** cmdlet 'ı bir Azure Yedekleme Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad064-106">The **New-AzureRmBackupVault** cmdlet creates an Azure Backup vault.</span></span>
<span data-ttu-id="ad064-107">Bu cmdlet, kasa varlığına başvuru olarak davranan bir **Azurermbackupkasa** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="ad064-107">This cmdlet returns an **AzureRmBackupVault** object that acts as a reference to the vault entity.</span></span>

## <span data-ttu-id="ad064-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad064-108">EXAMPLES</span></span>

### <span data-ttu-id="ad064-109">Örnek 1: yedek Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="ad064-109">Example 1: Create a backup vault</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="ad064-110">Bu komut, Vault03 adında bir Azure Yedekleme Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad064-110">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="ad064-111">Kasa, Batı ABD bölgesindeki ResourceGroup01 adlı kaynak grubudur.</span><span class="sxs-lookup"><span data-stu-id="ad064-111">The vault is in the resource group named ResourceGroup01 in the West US region.</span></span>
<span data-ttu-id="ad064-112">Kasa, varsayılan Geoyedekli depolama türünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="ad064-112">The vault uses the default GeoRedundant storage type.</span></span>

### <span data-ttu-id="ad064-113">Örnek 2: yerel olarak yedekli depolama kullanan bir yedek Kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="ad064-113">Example 2: Create a backup vault that uses locally redundant storage</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

<span data-ttu-id="ad064-114">Bu komut, Vault03 adında bir Azure Yedekleme Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad064-114">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="ad064-115">Kasa, Batı ABD bölgesindeki ResourceGroup02 adlı kaynak grubudur.</span><span class="sxs-lookup"><span data-stu-id="ad064-115">The vault is in the resource group named ResourceGroup02 in the West US region.</span></span>
<span data-ttu-id="ad064-116">Kasa, Locallyyedekli depolama türünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="ad064-116">The vault uses the LocallyRedundant storage type.</span></span>

## <span data-ttu-id="ad064-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad064-117">PARAMETERS</span></span>

### <span data-ttu-id="ad064-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad064-118">-Name</span></span>
<span data-ttu-id="ad064-119">Azure Yedekleme Kasası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad064-119">Specifies a name for the Azure Backup vault.</span></span>
<span data-ttu-id="ad064-120">Ad, kaynak grubunda benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ad064-120">The name must be unique in a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad064-121">-Bölge</span><span class="sxs-lookup"><span data-stu-id="ad064-121">-Region</span></span>
<span data-ttu-id="ad064-122">Yedek kasanın olduğu bir Azure bölgesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad064-122">Specifies an Azure region in which the backup vault exists.</span></span>
<span data-ttu-id="ad064-123">Karma yedekleme senaryolarında, gecikme süresini azaltmak için bir bölgede şirket içi sunucusuna bir kasa oluşturmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="ad064-123">For hybrid backup scenarios, we recommend that you create a vault in a region close to the on-premise server to reduce latency.</span></span>
<span data-ttu-id="ad064-124">Azure altyapısının hizmet (IaaS) sanal makineleri yedeklemesi için, kasa yerel sanal makinelerin keşif noktası olur.</span><span class="sxs-lookup"><span data-stu-id="ad064-124">For backup of Azure infrastructure as a service (IaaS) virtual machines, the vault becomes the point of discovery for local virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad064-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad064-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad064-126">Bu cmdlet 'in yedek Kasası oluşturduğu mevcut bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad064-126">Specifies the name of an existing Azure resource group in which this cmdlet creates a Backup vault.</span></span>
<span data-ttu-id="ad064-127">Kaynak grubu oluşturmak için New-AzureRMResourceGroup cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ad064-127">To create a resource group, use the New-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="ad064-128">Kaynak grubunun ve Azure yedekleme kasasındaki aynı bölgede olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="ad064-128">The resource group and the Azure Backup vault do not have to be in the same region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad064-129">-Depolama</span><span class="sxs-lookup"><span data-stu-id="ad064-129">-Storage</span></span>
<span data-ttu-id="ad064-130">Yedekleme verileri için depolama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad064-130">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="ad064-131">Bu parametre için kabul edilebilir değerler: Locallyyedekli ve Geoyedekli.</span><span class="sxs-lookup"><span data-stu-id="ad064-131">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>
<span data-ttu-id="ad064-132">Varsayılan değer Geoyedekli değeridir.</span><span class="sxs-lookup"><span data-stu-id="ad064-132">The default value is GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad064-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad064-133">-DefaultProfile</span></span>
<span data-ttu-id="ad064-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad064-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad064-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad064-135">CommonParameters</span></span>
<span data-ttu-id="ad064-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad064-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad064-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad064-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad064-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad064-138">INPUTS</span></span>

### <span data-ttu-id="ad064-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ad064-139">None</span></span>

## <span data-ttu-id="ad064-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad064-140">OUTPUTS</span></span>

### <span data-ttu-id="ad064-141">Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="ad064-141">AzureRmBackupVault</span></span>

## <span data-ttu-id="ad064-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad064-142">NOTES</span></span>
* <span data-ttu-id="ad064-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ad064-143">None</span></span>

## <span data-ttu-id="ad064-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad064-144">RELATED LINKS</span></span>

[<span data-ttu-id="ad064-145">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="ad064-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ad064-146">Remove-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="ad064-146">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="ad064-147">Set-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="ad064-147">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


