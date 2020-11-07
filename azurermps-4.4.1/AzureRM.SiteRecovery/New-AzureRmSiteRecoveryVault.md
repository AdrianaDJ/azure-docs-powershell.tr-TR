---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 786e3c17ca64acf908d06b88462f44af502e36c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762684"
---
# <span data-ttu-id="8b037-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="8b037-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="8b037-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b037-102">SYNOPSIS</span></span>
<span data-ttu-id="8b037-103">Site Recovery Services Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b037-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b037-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b037-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b037-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b037-105">DESCRIPTION</span></span>
<span data-ttu-id="8b037-106">**New-AzureRmSiteRecoveryVault** cmdlet 'ı bir Azure Site Recovery Services Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b037-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="8b037-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b037-107">EXAMPLES</span></span>

## <span data-ttu-id="8b037-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b037-108">PARAMETERS</span></span>

### <span data-ttu-id="8b037-109">-Konum</span><span class="sxs-lookup"><span data-stu-id="8b037-109">-Location</span></span>
<span data-ttu-id="8b037-110">Coğrafi konum adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b037-110">Specifies the geographical location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b037-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b037-111">-Name</span></span>
<span data-ttu-id="8b037-112">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b037-112">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b037-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b037-113">-ResourceGroupName</span></span>
<span data-ttu-id="8b037-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b037-114">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b037-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b037-115">-DefaultProfile</span></span>
<span data-ttu-id="8b037-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b037-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b037-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b037-117">CommonParameters</span></span>
<span data-ttu-id="8b037-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b037-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b037-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b037-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b037-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b037-120">INPUTS</span></span>

## <span data-ttu-id="8b037-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b037-121">OUTPUTS</span></span>

## <span data-ttu-id="8b037-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b037-122">NOTES</span></span>

## <span data-ttu-id="8b037-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b037-123">RELATED LINKS</span></span>

[<span data-ttu-id="8b037-124">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="8b037-124">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="8b037-125">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="8b037-125">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
