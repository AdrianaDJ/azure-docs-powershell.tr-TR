---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: d541c943c8dc9779cdf340440078ca2fd2fb36e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935250"
---
# <span data-ttu-id="b4607-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="b4607-101">Get-AzProfile</span></span>

## <span data-ttu-id="b4607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4607-102">SYNOPSIS</span></span>
<span data-ttu-id="b4607-103">Yüklü modüller tarafından desteklenen hizmet profillerini edinin.</span><span class="sxs-lookup"><span data-stu-id="b4607-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="b4607-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4607-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="b4607-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4607-105">DESCRIPTION</span></span>
<span data-ttu-id="b4607-106">Yüklü modüller tarafından desteklenen hizmet profillerini edinin.</span><span class="sxs-lookup"><span data-stu-id="b4607-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="b4607-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4607-107">EXAMPLES</span></span>

### <span data-ttu-id="b4607-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4607-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="b4607-109">Tuş Kasası modülü tarafından desteklenen hizmet profilini alma</span><span class="sxs-lookup"><span data-stu-id="b4607-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="b4607-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4607-110">PARAMETERS</span></span>

### <span data-ttu-id="b4607-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="b4607-111">-ListAvailable</span></span>
<span data-ttu-id="b4607-112">Yüklü modüller tarafından desteklenen tüm hizmet profillerinin listesi</span><span class="sxs-lookup"><span data-stu-id="b4607-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="b4607-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="b4607-113">-ModuleName</span></span>
<span data-ttu-id="b4607-114">Denetlenecek modülün adı</span><span class="sxs-lookup"><span data-stu-id="b4607-114">The name of the module to check</span></span>

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

### <span data-ttu-id="b4607-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4607-115">CommonParameters</span></span>
<span data-ttu-id="b4607-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4607-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4607-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b4607-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4607-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4607-118">INPUTS</span></span>

### <span data-ttu-id="b4607-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b4607-119">None</span></span>

## <span data-ttu-id="b4607-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4607-120">OUTPUTS</span></span>

### <span data-ttu-id="b4607-121">Microsoft. Azure. Commands. Profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="b4607-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="b4607-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4607-122">NOTES</span></span>

## <span data-ttu-id="b4607-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4607-123">RELATED LINKS</span></span>
