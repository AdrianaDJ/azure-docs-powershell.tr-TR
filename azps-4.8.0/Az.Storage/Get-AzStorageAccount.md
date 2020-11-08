---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110184"
---
# <span data-ttu-id="3b0c5-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3b0c5-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="3b0c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="3b0c5-103">Depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-103">Gets a Storage account.</span></span>

## <span data-ttu-id="3b0c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b0c5-104">SYNTAX</span></span>

### <span data-ttu-id="3b0c5-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b0c5-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b0c5-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b0c5-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b0c5-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b0c5-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b0c5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b0c5-108">DESCRIPTION</span></span>
<span data-ttu-id="3b0c5-109">**Get-AzStorageAccount** cmdlet 'i, bir kaynak grubundaki veya abonelikteki tüm depolama hesabını veya depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="3b0c5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b0c5-110">EXAMPLES</span></span>

### <span data-ttu-id="3b0c5-111">Örnek 1: belirtilen depolama hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="3b0c5-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="3b0c5-112">Bu komut belirtilen depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="3b0c5-113">Örnek 2: kaynak grubundaki tüm depolama hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="3b0c5-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="3b0c5-114">Bu komut, kaynak grubundaki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="3b0c5-115">Örnek 3: abonelikteki tüm depolama hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="3b0c5-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="3b0c5-116">Bu komut, abonelikteki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="3b0c5-117">Örnek 4: blob geri yükleme durumuyla depolama hesapları alma</span><span class="sxs-lookup"><span data-stu-id="3b0c5-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="3b0c5-118">Bu komut, blob geri yükleme durumunu içeren bir depolama hesabı alır ve BLOB geri yükleme durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="3b0c5-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b0c5-119">PARAMETERS</span></span>

### <span data-ttu-id="3b0c5-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="3b0c5-120">-AsJob</span></span>
<span data-ttu-id="3b0c5-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3b0c5-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0c5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b0c5-122">-DefaultProfile</span></span>
<span data-ttu-id="3b0c5-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b0c5-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="3b0c5-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="3b0c5-125">Depolama hesabının BlobRestoreStatus edinin.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-125">Get the BlobRestoreStatus of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0c5-126">-Includegeoreplicationstats</span><span class="sxs-lookup"><span data-stu-id="3b0c5-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="3b0c5-127">Depolama hesabının GeoReplicationStats öğesini edinin.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-127">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0c5-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b0c5-128">-Name</span></span>
<span data-ttu-id="3b0c5-129">Alınacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-129">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0c5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b0c5-130">-ResourceGroupName</span></span>
<span data-ttu-id="3b0c5-131">Alınacak depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b0c5-132">CommonParameters</span></span>
<span data-ttu-id="3b0c5-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b0c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b0c5-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b0c5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b0c5-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b0c5-135">INPUTS</span></span>

### <span data-ttu-id="3b0c5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3b0c5-136">System.String</span></span>

## <span data-ttu-id="3b0c5-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b0c5-137">OUTPUTS</span></span>

### <span data-ttu-id="3b0c5-138">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3b0c5-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="3b0c5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b0c5-139">NOTES</span></span>

## <span data-ttu-id="3b0c5-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b0c5-140">RELATED LINKS</span></span>

[<span data-ttu-id="3b0c5-141">Yeni-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3b0c5-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="3b0c5-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3b0c5-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="3b0c5-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3b0c5-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


