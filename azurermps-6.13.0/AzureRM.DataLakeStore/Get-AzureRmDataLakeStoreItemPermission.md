---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 6aeae8333cc8aa5a394abfaba68dcc0d7fb732f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588486"
---
# <span data-ttu-id="4cebd-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="4cebd-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="4cebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cebd-102">SYNOPSIS</span></span>
<span data-ttu-id="4cebd-103">Data Lake Store 'da bir dosya veya klasörün sekizlik miktarını alır.</span><span class="sxs-lookup"><span data-stu-id="4cebd-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cebd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4cebd-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cebd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4cebd-105">DESCRIPTION</span></span>
<span data-ttu-id="4cebd-106">**Get-AzureRmDataLakeStoreItemPermission** cmdlet 'ı, Data Lake Store 'da bir dosya veya klasörün sekizlik olduğunu alır.</span><span class="sxs-lookup"><span data-stu-id="4cebd-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4cebd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4cebd-107">EXAMPLES</span></span>

### <span data-ttu-id="4cebd-108">Örnek 1: dosyanın sekizlik olduğunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="4cebd-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="4cebd-109">Bu komut, bir dosya için sekizlik izni alır.</span><span class="sxs-lookup"><span data-stu-id="4cebd-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="4cebd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4cebd-110">PARAMETERS</span></span>

### <span data-ttu-id="4cebd-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="4cebd-111">-Account</span></span>
<span data-ttu-id="4cebd-112">Data Lake Store hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cebd-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="4cebd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cebd-113">-DefaultProfile</span></span>
<span data-ttu-id="4cebd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4cebd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cebd-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="4cebd-115">-Path</span></span>
<span data-ttu-id="4cebd-116">Kök dizinden (/) başlayarak dosya veya klasörün veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cebd-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4cebd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cebd-117">CommonParameters</span></span>
<span data-ttu-id="4cebd-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cebd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cebd-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cebd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cebd-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4cebd-120">INPUTS</span></span>

### <span data-ttu-id="4cebd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4cebd-121">System.String</span></span>

### <span data-ttu-id="4cebd-122">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4cebd-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="4cebd-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4cebd-123">OUTPUTS</span></span>

### <span data-ttu-id="4cebd-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4cebd-124">System.String</span></span>
<span data-ttu-id="4cebd-125">Sahip sekizlik 'ın dize gösterimi</span><span class="sxs-lookup"><span data-stu-id="4cebd-125">The string representation of the ownership octal</span></span>

## <span data-ttu-id="4cebd-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4cebd-126">NOTES</span></span>
* <span data-ttu-id="4cebd-127">Diğer ad: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="4cebd-127">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="4cebd-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4cebd-128">RELATED LINKS</span></span>

[<span data-ttu-id="4cebd-129">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="4cebd-129">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


