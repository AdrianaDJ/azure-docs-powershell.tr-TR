---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 75ec5690c3699ce8812383ddd128803bf662e489
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934067"
---
# <span data-ttu-id="0b58a-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0b58a-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="0b58a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b58a-102">SYNOPSIS</span></span>
<span data-ttu-id="0b58a-103">Azure depolama hesabı için erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0b58a-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="0b58a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b58a-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b58a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b58a-105">DESCRIPTION</span></span>
<span data-ttu-id="0b58a-106">**Get-AzStorageAccountKey** cmdlet 'ı bir Azure depolama hesabının erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0b58a-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="0b58a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b58a-107">EXAMPLES</span></span>

### <span data-ttu-id="0b58a-108">Örnek 1: depolama hesabının erişim anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="0b58a-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="0b58a-109">Bu komut belirtilen Azure depolama hesabı için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="0b58a-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="0b58a-110">Örnek 2: depolama hesabı için belirli bir erişim anahtarı alma</span><span class="sxs-lookup"><span data-stu-id="0b58a-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="0b58a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b58a-111">PARAMETERS</span></span>

### <span data-ttu-id="0b58a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b58a-112">-DefaultProfile</span></span>
<span data-ttu-id="0b58a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b58a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b58a-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b58a-114">-Name</span></span>
<span data-ttu-id="0b58a-115">Bu cmdlet 'in anahtarları aldığı depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b58a-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b58a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b58a-116">-ResourceGroupName</span></span>
<span data-ttu-id="0b58a-117">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b58a-117">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b58a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b58a-118">CommonParameters</span></span>
<span data-ttu-id="0b58a-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b58a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b58a-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b58a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b58a-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b58a-121">INPUTS</span></span>

### <span data-ttu-id="0b58a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="0b58a-122">System.String</span></span>

## <span data-ttu-id="0b58a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b58a-123">OUTPUTS</span></span>

### <span data-ttu-id="0b58a-124">Microsoft. Azure. Management. Storage. model. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0b58a-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="0b58a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b58a-125">NOTES</span></span>

## <span data-ttu-id="0b58a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b58a-126">RELATED LINKS</span></span>

[<span data-ttu-id="0b58a-127">Yeni-Azstoragekey</span><span class="sxs-lookup"><span data-stu-id="0b58a-127">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


