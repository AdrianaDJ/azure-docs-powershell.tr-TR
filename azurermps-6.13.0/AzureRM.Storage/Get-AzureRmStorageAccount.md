---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: bf63046ebe8b73f97a80e1465060b6265f99923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762088"
---
# <span data-ttu-id="542f3-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="542f3-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="542f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="542f3-102">SYNOPSIS</span></span>
<span data-ttu-id="542f3-103">Depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="542f3-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="542f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="542f3-104">SYNTAX</span></span>

### <span data-ttu-id="542f3-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="542f3-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="542f3-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="542f3-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="542f3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="542f3-107">DESCRIPTION</span></span>
<span data-ttu-id="542f3-108">**Get-AzureRmStorageAccount** cmdlet 'i, belirli bir depolama hesabını veya bir kaynak grubundaki veya abonelikteki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="542f3-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="542f3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="542f3-109">EXAMPLES</span></span>

### <span data-ttu-id="542f3-110">Örnek 1: belirtilen depolama hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="542f3-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="542f3-111">Bu komut belirtilen depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="542f3-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="542f3-112">Örnek 2: kaynak grubundaki tüm depolama hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="542f3-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="542f3-113">Bu komut, kaynak grubundaki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="542f3-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="542f3-114">Örnek 3: abonelikteki tüm depolama hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="542f3-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="542f3-115">Bu komut, abonelikteki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="542f3-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="542f3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="542f3-116">PARAMETERS</span></span>

### <span data-ttu-id="542f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542f3-117">-DefaultProfile</span></span>
<span data-ttu-id="542f3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="542f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="542f3-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="542f3-119">-Name</span></span>
<span data-ttu-id="542f3-120">Alınacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="542f3-120">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="542f3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="542f3-121">-ResourceGroupName</span></span>
<span data-ttu-id="542f3-122">Alınacak depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="542f3-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="542f3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542f3-123">CommonParameters</span></span>
<span data-ttu-id="542f3-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="542f3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542f3-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="542f3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542f3-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="542f3-126">INPUTS</span></span>

### <span data-ttu-id="542f3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="542f3-127">System.String</span></span>

## <span data-ttu-id="542f3-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="542f3-128">OUTPUTS</span></span>

### <span data-ttu-id="542f3-129">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="542f3-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="542f3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="542f3-130">NOTES</span></span>

## <span data-ttu-id="542f3-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="542f3-131">RELATED LINKS</span></span>

[<span data-ttu-id="542f3-132">Yeni-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="542f3-132">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="542f3-133">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="542f3-133">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="542f3-134">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="542f3-134">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


