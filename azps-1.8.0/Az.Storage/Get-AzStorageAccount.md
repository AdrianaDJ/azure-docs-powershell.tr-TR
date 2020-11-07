---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ba81e987e19d6698c8ea1d9e489d353d58007aea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758686"
---
# <span data-ttu-id="d79b0-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d79b0-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="d79b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d79b0-102">SYNOPSIS</span></span>
<span data-ttu-id="d79b0-103">Depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="d79b0-103">Gets a Storage account.</span></span>

## <span data-ttu-id="d79b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d79b0-104">SYNTAX</span></span>

### <span data-ttu-id="d79b0-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d79b0-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d79b0-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d79b0-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d79b0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d79b0-107">DESCRIPTION</span></span>
<span data-ttu-id="d79b0-108">**Get-AzStorageAccount** cmdlet 'i, bir kaynak grubundaki veya abonelikteki tüm depolama hesabını veya depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d79b0-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="d79b0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d79b0-109">EXAMPLES</span></span>

### <span data-ttu-id="d79b0-110">Örnek 1: belirtilen depolama hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="d79b0-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="d79b0-111">Bu komut belirtilen depolama hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="d79b0-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="d79b0-112">Örnek 2: kaynak grubundaki tüm depolama hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="d79b0-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="d79b0-113">Bu komut, kaynak grubundaki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d79b0-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="d79b0-114">Örnek 3: abonelikteki tüm depolama hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="d79b0-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="d79b0-115">Bu komut, abonelikteki tüm depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d79b0-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="d79b0-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d79b0-116">PARAMETERS</span></span>

### <span data-ttu-id="d79b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79b0-117">-DefaultProfile</span></span>
<span data-ttu-id="d79b0-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d79b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d79b0-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d79b0-119">-Name</span></span>
<span data-ttu-id="d79b0-120">Alınacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79b0-120">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="d79b0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d79b0-121">-ResourceGroupName</span></span>
<span data-ttu-id="d79b0-122">Alınacak depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79b0-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="d79b0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79b0-123">CommonParameters</span></span>
<span data-ttu-id="d79b0-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d79b0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79b0-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79b0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79b0-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d79b0-126">INPUTS</span></span>

### <span data-ttu-id="d79b0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d79b0-127">System.String</span></span>

## <span data-ttu-id="d79b0-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d79b0-128">OUTPUTS</span></span>

### <span data-ttu-id="d79b0-129">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d79b0-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d79b0-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d79b0-130">NOTES</span></span>

## <span data-ttu-id="d79b0-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d79b0-131">RELATED LINKS</span></span>

[<span data-ttu-id="d79b0-132">Yeni-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d79b0-132">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="d79b0-133">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d79b0-133">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="d79b0-134">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d79b0-134">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


