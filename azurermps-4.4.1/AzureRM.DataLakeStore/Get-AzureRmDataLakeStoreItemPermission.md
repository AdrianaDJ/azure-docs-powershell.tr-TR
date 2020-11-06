---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 1743ee6e4d0ce1276c69bec9e3669b5d04ee3858
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593148"
---
# <span data-ttu-id="d4b11-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d4b11-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="d4b11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4b11-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b11-103">Data Lake Store 'da bir dosya veya klasörün sekizlik miktarını alır.</span><span class="sxs-lookup"><span data-stu-id="d4b11-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4b11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4b11-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4b11-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4b11-105">DESCRIPTION</span></span>
<span data-ttu-id="d4b11-106">**Get-AzureRmDataLakeStoreItemPermission** cmdlet 'ı, Data Lake Store 'da bir dosya veya klasörün sekizlik olduğunu alır.</span><span class="sxs-lookup"><span data-stu-id="d4b11-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d4b11-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4b11-107">EXAMPLES</span></span>

### <span data-ttu-id="d4b11-108">Örnek 1: dosyanın sekizlik olduğunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="d4b11-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="d4b11-109">Bu komut, bir dosya için sekizlik izni alır.</span><span class="sxs-lookup"><span data-stu-id="d4b11-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="d4b11-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4b11-110">PARAMETERS</span></span>

### <span data-ttu-id="d4b11-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="d4b11-111">-Account</span></span>
<span data-ttu-id="d4b11-112">Data Lake Store hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4b11-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b11-113">-Yol</span><span class="sxs-lookup"><span data-stu-id="d4b11-113">-Path</span></span>
<span data-ttu-id="d4b11-114">Kök dizinden (/) başlayarak dosya veya klasörün veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4b11-114">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b11-115">-DefaultProfile</span></span>
<span data-ttu-id="d4b11-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4b11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4b11-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b11-117">CommonParameters</span></span>
<span data-ttu-id="d4b11-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4b11-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b11-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4b11-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b11-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4b11-120">INPUTS</span></span>

## <span data-ttu-id="d4b11-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4b11-121">OUTPUTS</span></span>

### <span data-ttu-id="d4b11-122">dizisi</span><span class="sxs-lookup"><span data-stu-id="d4b11-122">string</span></span>
<span data-ttu-id="d4b11-123">Sahip sekizlik 'ın dize gösterimi</span><span class="sxs-lookup"><span data-stu-id="d4b11-123">The string representation of the ownership octal</span></span>

## <span data-ttu-id="d4b11-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4b11-124">NOTES</span></span>
* <span data-ttu-id="d4b11-125">Diğer ad: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d4b11-125">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="d4b11-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4b11-126">RELATED LINKS</span></span>

[<span data-ttu-id="d4b11-127">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d4b11-127">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


