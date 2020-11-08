---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 165a85f48bc39608bd636073b4b12427e0a81bf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098493"
---
# <span data-ttu-id="04ba4-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="04ba4-101">Get-AzProfile</span></span>

## <span data-ttu-id="04ba4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="04ba4-103">Yüklü modüller tarafından desteklenen hizmet profillerini edinin.</span><span class="sxs-lookup"><span data-stu-id="04ba4-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="04ba4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04ba4-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="04ba4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="04ba4-105">DESCRIPTION</span></span>
<span data-ttu-id="04ba4-106">Yüklü modüller tarafından desteklenen hizmet profillerini edinin.</span><span class="sxs-lookup"><span data-stu-id="04ba4-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="04ba4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04ba4-107">EXAMPLES</span></span>

### <span data-ttu-id="04ba4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="04ba4-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="04ba4-109">Tuş Kasası modülü tarafından desteklenen hizmet profilini alma</span><span class="sxs-lookup"><span data-stu-id="04ba4-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="04ba4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04ba4-110">PARAMETERS</span></span>

### <span data-ttu-id="04ba4-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="04ba4-111">-ListAvailable</span></span>
<span data-ttu-id="04ba4-112">Yüklü modüller tarafından desteklenen tüm hizmet profillerinin listesi</span><span class="sxs-lookup"><span data-stu-id="04ba4-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="04ba4-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="04ba4-113">-ModuleName</span></span>
<span data-ttu-id="04ba4-114">Denetlenecek modülün adı</span><span class="sxs-lookup"><span data-stu-id="04ba4-114">The name of the module to check</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ba4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ba4-115">CommonParameters</span></span>
<span data-ttu-id="04ba4-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04ba4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ba4-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ba4-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ba4-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04ba4-118">INPUTS</span></span>

### <span data-ttu-id="04ba4-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="04ba4-119">None</span></span>

## <span data-ttu-id="04ba4-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04ba4-120">OUTPUTS</span></span>

### <span data-ttu-id="04ba4-121">Microsoft. Azure. Commands. Profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="04ba4-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="04ba4-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04ba4-122">NOTES</span></span>

## <span data-ttu-id="04ba4-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04ba4-123">RELATED LINKS</span></span>
