---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: db0c0672a6f60aa8c46f85a98e74f5184842cd72
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097777"
---
# <span data-ttu-id="d84e7-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d84e7-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="d84e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d84e7-102">SYNOPSIS</span></span>
<span data-ttu-id="d84e7-103">Depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="d84e7-103">Gets a Storage account.</span></span>

## <span data-ttu-id="d84e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d84e7-104">SYNTAX</span></span>

### <span data-ttu-id="d84e7-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d84e7-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d84e7-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d84e7-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d84e7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d84e7-107">DESCRIPTION</span></span>
<span data-ttu-id="d84e7-108">**Get-AzStorageAccount** cmdlet 'i, bir kaynak grubundaki veya abonelikteki tüm depolama hesabını veya depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d84e7-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="d84e7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d84e7-109">EXAMPLES</span></span>

### <span data-ttu-id="d84e7-110">Örnek 1: belirtilen depolama hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="d84e7-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="d84e7-111">Bu komut belirtilen depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="d84e7-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="d84e7-112">Örnek 2: kaynak grubundaki tüm depolama hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="d84e7-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="d84e7-113">Bu komut, kaynak grubundaki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d84e7-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="d84e7-114">Örnek 3: abonelikteki tüm depolama hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="d84e7-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="d84e7-115">Bu komut, abonelikteki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d84e7-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="d84e7-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d84e7-116">PARAMETERS</span></span>

### <span data-ttu-id="d84e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84e7-117">-DefaultProfile</span></span>
<span data-ttu-id="d84e7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d84e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d84e7-119">-Includegeoreplicationstats</span><span class="sxs-lookup"><span data-stu-id="d84e7-119">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="d84e7-120">Depolama hesabının GeoReplicationStats öğesini edinin.</span><span class="sxs-lookup"><span data-stu-id="d84e7-120">Get the GeoReplicationStats of the Storage account.</span></span>

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

### <span data-ttu-id="d84e7-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d84e7-121">-Name</span></span>
<span data-ttu-id="d84e7-122">Alınacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d84e7-122">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84e7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d84e7-123">-ResourceGroupName</span></span>
<span data-ttu-id="d84e7-124">Alınacak depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d84e7-124">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84e7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84e7-125">CommonParameters</span></span>
<span data-ttu-id="d84e7-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d84e7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84e7-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d84e7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84e7-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d84e7-128">INPUTS</span></span>

### <span data-ttu-id="d84e7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d84e7-129">System.String</span></span>

## <span data-ttu-id="d84e7-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d84e7-130">OUTPUTS</span></span>

### <span data-ttu-id="d84e7-131">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d84e7-131">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d84e7-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d84e7-132">NOTES</span></span>

## <span data-ttu-id="d84e7-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d84e7-133">RELATED LINKS</span></span>

[<span data-ttu-id="d84e7-134">Yeni-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d84e7-134">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="d84e7-135">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d84e7-135">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="d84e7-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d84e7-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


