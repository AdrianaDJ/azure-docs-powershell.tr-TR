---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AFD3971-460D-4F6A-B266-6ED98DC81CD4
online version: ''
schema: 2.0.0
ms.openlocfilehash: c007e3a318067f29da6ea710c25cf2c52d5df2b4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106239"
---
# <span data-ttu-id="f3bab-101">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f3bab-101">Move-AzureStorageAccount</span></span>

## <span data-ttu-id="f3bab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3bab-102">SYNOPSIS</span></span>
<span data-ttu-id="f3bab-103">Depolama hesabını Azure Resource Manager yığınına geçirir.</span><span class="sxs-lookup"><span data-stu-id="f3bab-103">Migrates a storage account to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="f3bab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3bab-104">SYNTAX</span></span>

### <span data-ttu-id="f3bab-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3bab-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Validate] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3bab-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3bab-106">AbortMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Abort] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3bab-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3bab-107">CommitMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Commit] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3bab-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3bab-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Prepare] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f3bab-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3bab-109">DESCRIPTION</span></span>
<span data-ttu-id="f3bab-110">**Taşıma-AzureStorageAccount** cmdlet 'i, bir depolama hesabını Azure Kaynak Yöneticisi yığınındaki kaynak grubuna geçirir.</span><span class="sxs-lookup"><span data-stu-id="f3bab-110">The **Move-AzureStorageAccount** cmdlet migrates a storage account to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="f3bab-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3bab-111">EXAMPLES</span></span>

### <span data-ttu-id="f3bab-112">Örnek 1: depolama hesabı geçişini hazırlama</span><span class="sxs-lookup"><span data-stu-id="f3bab-112">Example 1: Prepare storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Prepare -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="f3bab-113">Bu komut, bir Azure Resource Manager yığınına geçmek için ContosoStorageName adlı depolama hesabını hazırlar.</span><span class="sxs-lookup"><span data-stu-id="f3bab-113">This command prepares the storage account named ContosoStorageName for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="f3bab-114">Örnek 2: depolama hesabı geçişi 'ni başlatma</span><span class="sxs-lookup"><span data-stu-id="f3bab-114">Example 2: Start storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Commit -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="f3bab-115">Bu komut, ContosoStorageName adlı depolama hesabının Azure Resource Manager yığınına geçirilmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f3bab-115">This command starts migration of the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="f3bab-116">Örnek 3: depolama hesabı geçişini doğrulama</span><span class="sxs-lookup"><span data-stu-id="f3bab-116">Example 3: Validate storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Validate -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="f3bab-117">Bu komut, Contosostoraame adındaki depolama hesabının geçişini Azure Resource Manager yığınına doğrular.</span><span class="sxs-lookup"><span data-stu-id="f3bab-117">This command validates migration for the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="f3bab-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3bab-118">PARAMETERS</span></span>

### <span data-ttu-id="f3bab-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="f3bab-119">-Abort</span></span>
<span data-ttu-id="f3bab-120">Bu cmdlet 'in depolama hesabı geçişini iptal ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3bab-120">Indicates that this cmdlet cancels the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bab-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="f3bab-121">-Commit</span></span>
<span data-ttu-id="f3bab-122">Bu cmdlet 'in depolama hesabı geçişini başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3bab-122">Indicates that this cmdlet starts the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bab-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f3bab-123">-InformationAction</span></span>
<span data-ttu-id="f3bab-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3bab-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f3bab-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f3bab-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3bab-126">'A</span><span class="sxs-lookup"><span data-stu-id="f3bab-126">Continue</span></span>
- <span data-ttu-id="f3bab-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="f3bab-127">Ignore</span></span>
- <span data-ttu-id="f3bab-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f3bab-128">Inquire</span></span>
- <span data-ttu-id="f3bab-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f3bab-129">SilentlyContinue</span></span>
- <span data-ttu-id="f3bab-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f3bab-130">Stop</span></span>
- <span data-ttu-id="f3bab-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f3bab-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bab-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f3bab-132">-InformationVariable</span></span>
<span data-ttu-id="f3bab-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3bab-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bab-134">-Prepare</span><span class="sxs-lookup"><span data-stu-id="f3bab-134">-Prepare</span></span>
<span data-ttu-id="f3bab-135">Bu cmdlet 'in geçiş için depolama hesabını hazırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3bab-135">Indicates that this cmdlet prepares the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bab-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="f3bab-136">-Profile</span></span>
<span data-ttu-id="f3bab-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3bab-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3bab-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f3bab-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bab-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f3bab-139">-StorageAccountName</span></span>
<span data-ttu-id="f3bab-140">Bu cmdlet 'in geçirolduğu depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3bab-140">Specifies the name of the storage account that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3bab-141">-Doğrulama</span><span class="sxs-lookup"><span data-stu-id="f3bab-141">-Validate</span></span>
<span data-ttu-id="f3bab-142">Bu cmdlet 'in geçiş için depolama hesabını doğrulayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3bab-142">Specifies that this cmdlet validates the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bab-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3bab-143">CommonParameters</span></span>
<span data-ttu-id="f3bab-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3bab-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3bab-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3bab-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3bab-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3bab-146">INPUTS</span></span>

## <span data-ttu-id="f3bab-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3bab-147">OUTPUTS</span></span>

## <span data-ttu-id="f3bab-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3bab-148">NOTES</span></span>

## <span data-ttu-id="f3bab-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3bab-149">RELATED LINKS</span></span>

[<span data-ttu-id="f3bab-150">Taşı-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f3bab-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="f3bab-151">Taşı-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="f3bab-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="f3bab-152">Taşı-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3bab-152">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="f3bab-153">Taşı-AzureService</span><span class="sxs-lookup"><span data-stu-id="f3bab-153">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="f3bab-154">Taşı-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3bab-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


