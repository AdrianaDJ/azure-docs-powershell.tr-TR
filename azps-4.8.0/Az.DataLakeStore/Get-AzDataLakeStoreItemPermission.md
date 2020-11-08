---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274572"
---
# <span data-ttu-id="df5ff-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="df5ff-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="df5ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="df5ff-103">Data Lake Store 'da bir dosya veya klasörün sekizlik miktarını alır.</span><span class="sxs-lookup"><span data-stu-id="df5ff-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="df5ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df5ff-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df5ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df5ff-105">DESCRIPTION</span></span>
<span data-ttu-id="df5ff-106">**Get-AzDataLakeStoreItemPermission** cmdlet 'ı, Data Lake Store 'da bir dosya veya klasörün sekizlik olduğunu alır.</span><span class="sxs-lookup"><span data-stu-id="df5ff-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="df5ff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df5ff-107">EXAMPLES</span></span>

### <span data-ttu-id="df5ff-108">Örnek 1: dosyanın sekizlik olduğunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="df5ff-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="df5ff-109">Bu komut, bir dosya için sekizlik izni alır.</span><span class="sxs-lookup"><span data-stu-id="df5ff-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="df5ff-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df5ff-110">PARAMETERS</span></span>

### <span data-ttu-id="df5ff-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="df5ff-111">-Account</span></span>
<span data-ttu-id="df5ff-112">Data Lake Store hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df5ff-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="df5ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5ff-113">-DefaultProfile</span></span>
<span data-ttu-id="df5ff-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df5ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df5ff-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="df5ff-115">-Path</span></span>
<span data-ttu-id="df5ff-116">Kök dizinden (/) başlayarak dosya veya klasörün veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="df5ff-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="df5ff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5ff-117">CommonParameters</span></span>
<span data-ttu-id="df5ff-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df5ff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5ff-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df5ff-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5ff-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df5ff-120">INPUTS</span></span>

### <span data-ttu-id="df5ff-121">System. String</span><span class="sxs-lookup"><span data-stu-id="df5ff-121">System.String</span></span>

### <span data-ttu-id="df5ff-122">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="df5ff-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="df5ff-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df5ff-123">OUTPUTS</span></span>

### <span data-ttu-id="df5ff-124">System. String</span><span class="sxs-lookup"><span data-stu-id="df5ff-124">System.String</span></span>

## <span data-ttu-id="df5ff-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df5ff-125">NOTES</span></span>
* <span data-ttu-id="df5ff-126">Diğer ad: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="df5ff-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="df5ff-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df5ff-127">RELATED LINKS</span></span>

[<span data-ttu-id="df5ff-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="df5ff-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


