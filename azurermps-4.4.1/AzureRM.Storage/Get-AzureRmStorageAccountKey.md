---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: d12be29507f581f3e9a8d0de86d8a571a305908d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589944"
---
# <span data-ttu-id="591a1-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="591a1-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="591a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="591a1-102">SYNOPSIS</span></span>
<span data-ttu-id="591a1-103">Azure depolama hesabı için erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="591a1-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="591a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="591a1-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="591a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="591a1-105">DESCRIPTION</span></span>
<span data-ttu-id="591a1-106">**Get-AzureRmStorageAccountKey** cmdlet 'ı bir Azure depolama hesabının erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="591a1-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="591a1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="591a1-107">EXAMPLES</span></span>

### <span data-ttu-id="591a1-108">Örnek 1: depolama hesabının erişim anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="591a1-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="591a1-109">Bu komut belirtilen Azure depolama hesabı için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="591a1-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="591a1-110">Örnek 2: depolama hesabı için belirli bir erişim anahtarı alma</span><span class="sxs-lookup"><span data-stu-id="591a1-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="591a1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="591a1-111">PARAMETERS</span></span>

### <span data-ttu-id="591a1-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="591a1-112">-Name</span></span>
<span data-ttu-id="591a1-113">Bu cmdlet 'in anahtarları aldığı depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="591a1-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="591a1-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591a1-114">-ResourceGroupName</span></span>
<span data-ttu-id="591a1-115">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="591a1-115">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="591a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591a1-116">-DefaultProfile</span></span>
<span data-ttu-id="591a1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="591a1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="591a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591a1-118">CommonParameters</span></span>
<span data-ttu-id="591a1-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="591a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591a1-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="591a1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591a1-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="591a1-121">INPUTS</span></span>

## <span data-ttu-id="591a1-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="591a1-122">OUTPUTS</span></span>

## <span data-ttu-id="591a1-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="591a1-123">NOTES</span></span>

## <span data-ttu-id="591a1-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="591a1-124">RELATED LINKS</span></span>

[<span data-ttu-id="591a1-125">Yeni-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="591a1-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)


