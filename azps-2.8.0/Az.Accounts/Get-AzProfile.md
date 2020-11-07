---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 937683c8592bb814b7f6a6262ef095cbd8252c78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753728"
---
# <span data-ttu-id="f1c5a-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="f1c5a-101">Get-AzProfile</span></span>

## <span data-ttu-id="f1c5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c5a-103">Yüklü modüller tarafından desteklenen hizmet profillerini edinin.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="f1c5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1c5a-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="f1c5a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1c5a-105">DESCRIPTION</span></span>
<span data-ttu-id="f1c5a-106">Yüklü modüller tarafından desteklenen hizmet profillerini edinin.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="f1c5a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1c5a-107">EXAMPLES</span></span>

### <span data-ttu-id="f1c5a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f1c5a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="f1c5a-109">Tuş Kasası modülü tarafından desteklenen hizmet profilini alma</span><span class="sxs-lookup"><span data-stu-id="f1c5a-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="f1c5a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1c5a-110">PARAMETERS</span></span>

### <span data-ttu-id="f1c5a-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="f1c5a-111">-ListAvailable</span></span>
<span data-ttu-id="f1c5a-112">Yüklü modüller tarafından desteklenen tüm hizmet profillerinin listesi</span><span class="sxs-lookup"><span data-stu-id="f1c5a-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="f1c5a-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="f1c5a-113">-ModuleName</span></span>
<span data-ttu-id="f1c5a-114">Denetlenecek modülün adı</span><span class="sxs-lookup"><span data-stu-id="f1c5a-114">The name of the module to check</span></span>

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

### <span data-ttu-id="f1c5a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c5a-115">CommonParameters</span></span>
<span data-ttu-id="f1c5a-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c5a-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1c5a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c5a-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1c5a-118">INPUTS</span></span>

### <span data-ttu-id="f1c5a-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f1c5a-119">None</span></span>

## <span data-ttu-id="f1c5a-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1c5a-120">OUTPUTS</span></span>

### <span data-ttu-id="f1c5a-121">Microsoft. Azure. Commands. Profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="f1c5a-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="f1c5a-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1c5a-122">NOTES</span></span>

## <span data-ttu-id="f1c5a-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1c5a-123">RELATED LINKS</span></span>