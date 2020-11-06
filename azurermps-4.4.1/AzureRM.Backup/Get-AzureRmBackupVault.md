---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: ef4d8ca2e1fb21165281375b3d325f5fc8b6ceed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588285"
---
# <span data-ttu-id="727b5-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="727b5-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="727b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="727b5-102">SYNOPSIS</span></span>
<span data-ttu-id="727b5-103">Yedek Kasası alır.</span><span class="sxs-lookup"><span data-stu-id="727b5-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="727b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="727b5-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="727b5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="727b5-105">DESCRIPTION</span></span>
<span data-ttu-id="727b5-106">**Get-Azurermbackupkasa** cmdlet 'ı Azure yedek Kasası alır.</span><span class="sxs-lookup"><span data-stu-id="727b5-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="727b5-107">Bu cmdlet diğer cmdlet 'ler için **Azurermbackupkasa** nesneleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="727b5-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="727b5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="727b5-108">EXAMPLES</span></span>

### <span data-ttu-id="727b5-109">Örnek 1: tüm yedekleme örneklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="727b5-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="727b5-110">Bu komut tüm Azure yedekleme yerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="727b5-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="727b5-111">Örnek 2: Batı ABD 'de oluşturulan tüm kasa görünümü</span><span class="sxs-lookup"><span data-stu-id="727b5-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="727b5-112">Bu komut tüm yedekleme yerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="727b5-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="727b5-113">Komut, ardışık düzen işlecini kullanarak bunları Where-Object cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="727b5-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="727b5-114">Bu cmdlet, **bölgeyi bölge** özelliğine göre filtreler.</span><span class="sxs-lookup"><span data-stu-id="727b5-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="727b5-115">Daha fazla bilgi için yazın `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="727b5-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="727b5-116">Örnek 3: belirli bir kasa alma</span><span class="sxs-lookup"><span data-stu-id="727b5-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="727b5-117">Bu komut Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="727b5-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="727b5-118">Örnek 4: yerel olarak yedekli depolama alanı olan kasa sayısını sayma</span><span class="sxs-lookup"><span data-stu-id="727b5-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="727b5-119">Bu komut tüm Azure yedekleme yerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="727b5-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="727b5-120">Bu komut, sonuçları **depolama** özelliğine dayalı olarak filtreleyen **yere** geçirir.</span><span class="sxs-lookup"><span data-stu-id="727b5-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="727b5-121">Komut, Locallyyedekli değeri olan Measure-Object cmdlet 'ine sahip olan sonuçları sayar.</span><span class="sxs-lookup"><span data-stu-id="727b5-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="727b5-122">Daha fazla bilgi için yazın `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="727b5-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="727b5-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="727b5-123">PARAMETERS</span></span>

### <span data-ttu-id="727b5-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="727b5-124">-Name</span></span>
<span data-ttu-id="727b5-125">Bu cmdlet 'in aldığı yedek kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="727b5-125">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="727b5-126">Birden fazla yedek Kasası aynı ada sahipse, bu cmdlet bunları döndürür.</span><span class="sxs-lookup"><span data-stu-id="727b5-126">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="727b5-127">Benzersiz bir kasa almak için *Resourcegroupname* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="727b5-127">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="727b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="727b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="727b5-129">Bu cmdlet 'in yedek Kasası aldığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="727b5-129">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="727b5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="727b5-130">-DefaultProfile</span></span>
<span data-ttu-id="727b5-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="727b5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="727b5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="727b5-132">CommonParameters</span></span>
<span data-ttu-id="727b5-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="727b5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="727b5-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="727b5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="727b5-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="727b5-135">INPUTS</span></span>

## <span data-ttu-id="727b5-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="727b5-136">OUTPUTS</span></span>

### <span data-ttu-id="727b5-137">Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="727b5-137">AzureRmBackupVault</span></span>

## <span data-ttu-id="727b5-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="727b5-138">NOTES</span></span>
* <span data-ttu-id="727b5-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="727b5-139">None</span></span>

## <span data-ttu-id="727b5-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="727b5-140">RELATED LINKS</span></span>

[<span data-ttu-id="727b5-141">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="727b5-141">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="727b5-142">Yeni-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="727b5-142">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="727b5-143">Remove-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="727b5-143">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="727b5-144">Set-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="727b5-144">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


