---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: 6845e9db485133faf67e9a82875b199b6dd77dcf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915768"
---
# <span data-ttu-id="fcb5e-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="fcb5e-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="fcb5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcb5e-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb5e-103">Medya hizmetiyle ilişkili REST uç noktasına erişmek için önemli bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="fcb5e-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="fcb5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fcb5e-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcb5e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fcb5e-105">DESCRIPTION</span></span>
<span data-ttu-id="fcb5e-106">**Get-AzMediaServiceKey** cmdlet 'ı, Azure Medya hizmeti Ile Ilişkili representational durum aktarma (REST) uç noktasına erişmek için temel bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="fcb5e-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="fcb5e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fcb5e-107">EXAMPLES</span></span>

### <span data-ttu-id="fcb5e-108">Örnek 1: medya hizmetine erişim için temel bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="fcb5e-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="fcb5e-109">Bu komut, ResourceGroup001 adındaki kaynak grubuna ait MediaService001 adındaki medya hizmetine erişmeye yönelik anahtar bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="fcb5e-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="fcb5e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fcb5e-110">PARAMETERS</span></span>

### <span data-ttu-id="fcb5e-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fcb5e-111">-AccountName</span></span>
<span data-ttu-id="fcb5e-112">Bu cmdlet 'in medya hizmeti anahtarlarını aldığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcb5e-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb5e-113">-DefaultProfile</span></span>
<span data-ttu-id="fcb5e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fcb5e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcb5e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcb5e-115">-ResourceGroupName</span></span>
<span data-ttu-id="fcb5e-116">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcb5e-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="fcb5e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb5e-117">CommonParameters</span></span>
<span data-ttu-id="fcb5e-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fcb5e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb5e-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb5e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb5e-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fcb5e-120">INPUTS</span></span>

### <span data-ttu-id="fcb5e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="fcb5e-121">System.String</span></span>

## <span data-ttu-id="fcb5e-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fcb5e-122">OUTPUTS</span></span>

### <span data-ttu-id="fcb5e-123">Microsoft. Azure. Commands. Media. modeller. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="fcb5e-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="fcb5e-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fcb5e-124">NOTES</span></span>

## <span data-ttu-id="fcb5e-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fcb5e-125">RELATED LINKS</span></span>

[<span data-ttu-id="fcb5e-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="fcb5e-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


