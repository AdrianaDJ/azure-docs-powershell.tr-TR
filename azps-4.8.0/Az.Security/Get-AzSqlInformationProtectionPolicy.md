---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107632"
---
# <span data-ttu-id="cd535-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd535-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="cd535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd535-102">SYNOPSIS</span></span>
<span data-ttu-id="cd535-103">Etkin kiracı SQL bilgileri koruma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="cd535-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="cd535-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd535-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd535-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd535-105">DESCRIPTION</span></span>
<span data-ttu-id="cd535-106">Etkin kiracı SQL bilgileri koruma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="cd535-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="cd535-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd535-107">EXAMPLES</span></span>

### <span data-ttu-id="cd535-108">Örnekteki</span><span class="sxs-lookup"><span data-stu-id="cd535-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="cd535-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd535-109">PARAMETERS</span></span>

### <span data-ttu-id="cd535-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="cd535-110">-AsJob</span></span>
<span data-ttu-id="cd535-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cd535-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd535-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd535-112">-DefaultProfile</span></span>
<span data-ttu-id="cd535-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd535-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd535-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd535-114">CommonParameters</span></span>
<span data-ttu-id="cd535-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd535-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd535-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cd535-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd535-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd535-117">INPUTS</span></span>

### <span data-ttu-id="cd535-118">System. String</span><span class="sxs-lookup"><span data-stu-id="cd535-118">System.string</span></span>

## <span data-ttu-id="cd535-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd535-119">OUTPUTS</span></span>

### <span data-ttu-id="cd535-120">Microsoft. Azure. Commands. Securitcenter. model. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd535-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="cd535-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd535-121">NOTES</span></span>

## <span data-ttu-id="cd535-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd535-122">RELATED LINKS</span></span>
