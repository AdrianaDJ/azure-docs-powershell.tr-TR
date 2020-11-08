---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 165a85f48bc39608bd636073b4b12427e0a81bf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268903"
---
# <span data-ttu-id="bc8b2-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="bc8b2-101">Get-AzProfile</span></span>

## <span data-ttu-id="bc8b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc8b2-102">SYNOPSIS</span></span>
<span data-ttu-id="bc8b2-103">Yüklü modüller tarafından desteklenen hizmet profillerini edinin.</span><span class="sxs-lookup"><span data-stu-id="bc8b2-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="bc8b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc8b2-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="bc8b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc8b2-105">DESCRIPTION</span></span>
<span data-ttu-id="bc8b2-106">Yüklü modüller tarafından desteklenen hizmet profillerini edinin.</span><span class="sxs-lookup"><span data-stu-id="bc8b2-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="bc8b2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc8b2-107">EXAMPLES</span></span>

### <span data-ttu-id="bc8b2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc8b2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="bc8b2-109">Tuş Kasası modülü tarafından desteklenen hizmet profilini alma</span><span class="sxs-lookup"><span data-stu-id="bc8b2-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="bc8b2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc8b2-110">PARAMETERS</span></span>

### <span data-ttu-id="bc8b2-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="bc8b2-111">-ListAvailable</span></span>
<span data-ttu-id="bc8b2-112">Yüklü modüller tarafından desteklenen tüm hizmet profillerinin listesi</span><span class="sxs-lookup"><span data-stu-id="bc8b2-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="bc8b2-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="bc8b2-113">-ModuleName</span></span>
<span data-ttu-id="bc8b2-114">Denetlenecek modülün adı</span><span class="sxs-lookup"><span data-stu-id="bc8b2-114">The name of the module to check</span></span>

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

### <span data-ttu-id="bc8b2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc8b2-115">CommonParameters</span></span>
<span data-ttu-id="bc8b2-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc8b2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc8b2-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc8b2-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc8b2-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc8b2-118">INPUTS</span></span>

### <span data-ttu-id="bc8b2-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bc8b2-119">None</span></span>

## <span data-ttu-id="bc8b2-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc8b2-120">OUTPUTS</span></span>

### <span data-ttu-id="bc8b2-121">Microsoft. Azure. Commands. Profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="bc8b2-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="bc8b2-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc8b2-122">NOTES</span></span>

## <span data-ttu-id="bc8b2-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc8b2-123">RELATED LINKS</span></span>
